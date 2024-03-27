<script setup>
	import { onMounted, ref, watch, } from "vue";
	import axios from 'axios';

	import CardItem from './CardItem.vue'
	import Tabs from './Tabs.vue'
	import Search from './Search.vue'

	const items = ref([]);
	const searchQuery = ref('')
	const filterQuery = ref('');
	const filterBrendQuery = ref('');

	const onClickAdd = (e) => {
		e.preventDefault();
		alert('Добавити');
	}

	const fetchData = async (url) => {
		try {
			const { data } = await axios.get(url);
			items.value = data;
		} catch (err) {
			console.log(err);
		}
	};

	const setFilter = (query, brend) => {
		filterQuery.value = query;
		filterBrendQuery.value = brend;
		fetchData(buildUrl());
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
					:title="item.title"
					:imgUrl="item.imgUrl"
					:price="item.price"
					:sale="item.sale"
					:brend="item.brend"
					:desc="item.desc"
					:isAdded="false"
					:isFavorite="true"
					:onClickAdded="onClickAdd"
					:onClickFavorite="onClickAdd"
					/>
			</div>

		</div>
	</div>
</template>
