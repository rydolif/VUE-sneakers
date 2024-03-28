<script setup>
	const emit = defineEmits(['onClickRemove'])

	defineProps({
		id: Number,
		title: String,
		desc: String,
		brend: String,
		imgUrl: String,
		price: String,
		sale: String,
	})

</script>

<template>
	<div class="drawer__item">
		<button class="drawer__close" @click="emit('onClickRemove')">
			<svg width="24px" height="24px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M19.207 6.207a1 1 0 0 0-1.414-1.414L12 10.586 6.207 4.793a1 1 0 0 0-1.414 1.414L10.586 12l-5.793 5.793a1 1 0 1 0 1.414 1.414L12 13.414l5.793 5.793a1 1 0 0 0 1.414-1.414L13.414 12l5.793-5.793z" fill="#fff"/></svg>
		</button>
		<img :src="imgUrl" class="drawer__img" alt="">
		<div class="drawer__item_content">
			<p class="cards__item_name">{{ title }}</p>
			<p class="cards__item_brand">{{ brend }}</p>
			<p class="cards__item_text">{{ desc }}</p>
			<div class="drawer__item_price">
				<span class="cards__item_price--old">{{ price }} $</span>
				<span class="cards__item_price--sale">{{ sale }} $</span>
			</div>
		</div>
	</div>
</template>
