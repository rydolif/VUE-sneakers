<script setup>
	import { inject } from "vue";
	import DrawerItem from "./DrawerItem.vue";

	const  { cart, removeFromCart, addToCart } = inject('cart')

</script>
<template>
	<div class="drawer__list">
		<DrawerItem 
			v-for="item in cart"
			:key="item.id" 
			:title="item.title"
			:imgUrl="item.imgUrl"
			:price="item.price"
			:sale="item.sale"
			:brend="item.brend"
			:desc="item.desc"
			@onClickRemove="() => removeFromCart(item)"
		/>
	</div>
</template>
