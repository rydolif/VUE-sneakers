<script setup>
	const probs = defineProps({
		id: Number,
		title: String,
		desc: String,
		brend: String,
		imgUrl: String,
		price: String,
		sale: String,
		isFavorite: Boolean,
		isAdded: Boolean,
		onClickFavorite: Function,
		onClickAdded: Function,
	})
</script>

<template>

	<div class="cards__item">
		<div class="cards__item_img">
			<span 
				v-if="!isFavorite" 
				class="cards__item_label"
				@click="onClickFavorite"
				>
				<svg width="24px" height="24px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path   fill-rule="evenodd" clip-rule="evenodd" d="M12 6.00019C10.2006 3.90317 7.19377 3.2551 4.93923 5.17534C2.68468 7.09558 2.36727 10.3061 4.13778 12.5772C5.60984 14.4654 10.0648 18.4479 11.5249 19.7369C11.6882 19.8811 11.7699 19.9532 11.8652 19.9815C11.9483 20.0062 12.0393 20.0062 12.1225 19.9815C12.2178 19.9532 12.2994 19.8811 12.4628 19.7369C13.9229 18.4479 18.3778 14.4654 19.8499 12.5772C21.6204 10.3061 21.3417 7.07538 19.0484 5.17534C16.7551 3.2753 13.7994 3.90317 12 6.00019Z" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
				</svg>
			</span>
			<span 
				v-else 
				@click="onClickFavorite" 
				class="cards__item_label"
				>
				<svg width="24px" height="24px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path  fill="#fff" d="M2 9.1371C2 14 6.01943 16.5914 8.96173 18.9109C10 19.7294 11 20.5 12 20.5C13 20.5 14 19.7294 15.0383 18.9109C17.9806 16.5914 22 14 22 9.1371C22 4.27416 16.4998 0.825464 12 5.50063C7.50016 0.825464 2 4.27416 2 9.1371Z"/>
				</svg>
			</span>
			<img :src="imgUrl" alt="">
		</div>
		<div class="cards__item_description">
			<p class="cards__item_name">{{ title }}</p>
			<p class="cards__item_brand">{{ brend }}</p>
			<p class="cards__item_text">{{ desc }}</p>
			<p class="cards__item_price">
				<span class="cards__item_price--old">{{ price }} $</span>
				<span class="cards__item_price--sale">{{ sale }} $</span>
				<a 
					v-if="!isAdded"
					@click="onClickAdded"
					href="#" 
					class="cards__item_btn">Add to cart</a>
				<a 
					v-else 
					href="#" 
					@click="onClickAdded" 
					class="cards__item_btn">Add</a>
			</p>
		</div>
	</div>

</template>
