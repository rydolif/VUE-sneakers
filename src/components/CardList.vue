<script setup>
	import { onMounted, ref, watch } from "vue";
	import axios from 'axios';

	import CardItem from './CardItem.vue'
	const items = ref([]);

	defineProps({
			items: Array,
	});
	const onClickAdd = (e) => {
		e.preventDefault();
		alert('Добавити');
	}

	
	onMounted(async() => {
		try {
			const {data} = await axios.get('https://d2420e17532c114f.mokky.dev/CardItem')
			items.value = data;
		} catch {
			console.log(err)
		}
	})

	const onValided = async function (brend) {
		const activeElements = document.querySelectorAll('.active');
		activeElements.forEach(element => {
				element.classList.remove('active');
		});
		event.target.classList.add('active');
		if (brend) {
			try {
					const { data } = await axios.get('https://d2420e17532c114f.mokky.dev/CardItem?brend=' + brend);
					items.value = data;
			} catch (err) {
					console.error(err);
			}
		} else {
			try {
				const {data} = await axios.get('https://d2420e17532c114f.mokky.dev/CardItem')
				items.value = data;
			} catch {
				console.log(err)
			}
		}
	}


</script>

<template>
	<div class="cards">
		<div class="container">
			
			<div class="catalog__tabs">
				<ul>
					<li><a @click="onValided()" class="active">All</a></li>
					<li><a @click="onValided('Puma')" >Puma</a></li>
					<li><a @click="onValided('Nike')" >Nike</a></li>
					<li><a @click="onValided('New Balance')">New Balance</a></li>
					<li><a @click="onValided('Adidas')" >Adidas</a></li>
					<li><a @click="onValided('Converse')" >Converse</a></li>
				</ul>
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
