<script setup>
	import { onMounted, ref, watch, } from "vue";
	import axios from 'axios';

	import CardItem from './CardItem.vue'

	const items = ref([]);
	const searchQuery = ref('');
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

			<div class="cards__search question__form">
				<div class="question__form_line">
					<input v-model="searchQuery" type="text" placeholder="Search" />
				</div>
			</div>

			<div class="cards__filters">
				<div class="catalog__tabs">
					<ul>
						<li><a @click="setFilter('', '')" :class="{ active: filterQuery === '' && filterBrendQuery === '' }">All</a></li>
						<li><a @click="setFilter('-price', '')" :class="{ active: filterQuery === '-price' && filterBrendQuery === '' }">Dear</a></li>
						<li><a @click="setFilter('price', '')" :class="{ active: filterQuery === 'price' && filterBrendQuery === '' }">Cheap</a></li>
						<li><a @click="setFilter('sale', '')" :class="{ active: filterQuery === 'sale' && filterBrendQuery === '' }">Sale</a></li>
					</ul>
				</div>

				<div class="catalog__tabs">
					<ul>
						<li><a @click="setFilter('', 'Puma')" :class="{ active: filterBrendQuery === 'Puma' && filterQuery === '' }">Puma</a></li>
						<li><a @click="setFilter('', 'Nike')" :class="{ active: filterBrendQuery === 'Nike' && filterQuery === '' }">Nike</a></li>
						<li><a @click="setFilter('', 'New Balance')" :class="{ active: filterBrendQuery === 'New Balance' && filterQuery === '' }">New Balance</a></li>
						<li><a @click="setFilter('', 'Adidas')" :class="{ active: filterBrendQuery === 'Adidas' && filterQuery === '' }">Adidas</a></li>
						<li><a @click="setFilter('', 'Converse')" :class="{ active: filterBrendQuery === 'Converse' && filterQuery === '' }">Converse</a></li>
					</ul>
				</div>
			</div>

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
