<script setup>
	import { onMounted, ref, watch, provide, defineEmits } from "vue";
	import axios from 'axios';

	import CardItem from './CardItem.vue'
	import Tabs from './Tabs.vue'
	import Search from './Search.vue'

	const items = ref([]);
	const searchQuery = ref('');
	const filterQuery = ref('');
	const filterBrendQuery = ref('');
	const isDataLoaded = ref(false);

	const fetchData = async (url) => {
		try {
			const { data } = await axios.get(url);
			items.value = data.map(obj => ({
				...obj,
				isAdded: false,
				isFavorite: false
			}));
			fetchFavorites();
			isDataLoaded.value = true;
		} catch (err) {
			console.log(err);
		}
	};

	const setFilter = (query, brend) => {
		filterQuery.value = query;
		filterBrendQuery.value = brend;
		fetchData(buildUrl());
		fetchFavorites();
	};

	const buildUrl = () => {
		let url = 'https://d2420e17532c114f.mokky.dev/CardItem?';
		const title = searchQuery.value;
		const query = filterQuery.value;
		const brend = filterBrendQuery.value;

		if (title) {
			url += `title=*${title}*`;
		}
		if (query) {
			url += `${title ? '&' : ''}sortBy=${query}`;
		}
		if (brend) {
			url += `${(title || query) ? '&' : ''}brend=${brend}`;
		}

		return url;
	};

	const fetchFavorites = async () => {
		try {
			const { data: favorites } = await axios.get('https://d2420e17532c114f.mokky.dev/Favorite');

			items.value = items.value.map(item => {
				const favorite = favorites.find(favorite => favorite.parentId === item.id)
				if(!favorite) {
					return item;
				}

				return {
					...item,
					isFavorite: true,
					favoriteId: favorite.id,
				}
			})
		} catch (err) {
			console.log(err);
		}
	};

	const addToFavorite = async (item) => {
		try {
			if(!item.isFavorite){
				const obj = {
					parentId: item.id
				}
				const { data } = await axios.post('https://d2420e17532c114f.mokky.dev/Favorite', obj);
				item.isFavorite = true
				item.favoriteId = data.id
			} else {
				await axios.delete(`https://d2420e17532c114f.mokky.dev/Favorite/${item.favoriteId}`);
				item.isFavorite = false
				item.favoriteId = null
			}
		} catch (err) {
			console.log(err)
		}
	}

	onMounted(() => {
		fetchData(buildUrl());
	});

	watch(searchQuery, () => {
		fetchData(buildUrl());
	});

	watch(filterQuery, () => {
		setFilter(filterQuery.value, filterBrendQuery.value);
	});

	watch(filterBrendQuery, () => {
		setFilter(filterQuery.value, filterBrendQuery.value);
	});

	provide('addToFavorite', addToFavorite)
	const emit = defineEmits('addToCart')
</script>


<template>
	<div class="cards">
		<div class="container">

			<Search :searchQuery="searchQuery" @update:searchQuery="searchQuery = $event" />

			<Tabs
				:setFilter='setFilter'
				:filterQuery='filterQuery'
				:filterBrendQuery='filterBrendQuery'
			/>

			<div class="cards__list cards__slider--three-block">
				<CardItem 
					v-for="item in items"
					:key="item.id"
					:id="item.id"
					:title="item.title"
					:imgUrl="item.imgUrl"
					:price="item.price"
					:sale="item.sale"
					:brend="item.brend"
					:desc="item.desc"
					:onClickFavorite="() => addToFavorite(item)"
					:isFavorite="item.isFavorite"
					:onClickAdded="() => emit('addToCart', item)"
					:isAdded="item.isAdded"
				/>
			</div>

		</div>
	</div>
</template>
