<script setup>
	defineProps({
		setFilter: Function,
		filterQuery: String,
		filterBrendQuery: String,
	})
</script>

<template>
	
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
</template>