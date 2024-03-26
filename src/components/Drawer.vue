<script setup>
	const removeDrawer = (e) => {
		e.preventDefault()
		const drawer  = document.querySelector('.drawer')
		drawer.classList.remove('drawer--active')
	}
</script>

<template>
	<div class="drawer">
		<div class="drawer__wrap">

			<div class="drawer__title">
				<a href="#" class="drawer__arrow" @click="removeDrawer">
					<svg width="30px" height="20px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M7.68473 7.33186C8.07526 6.94134 8.07526 6.30817 7.68473 5.91765C7.29421 5.52712 6.66105 5.52712 6.27052 5.91765L1.60492 10.5832C0.823873 11.3643 0.823872 12.6306 1.60492 13.4117L6.27336 18.0801C6.66388 18.4706 7.29705 18.4706 7.68757 18.0801C8.0781 17.6896 8.0781 17.0564 7.68757 16.6659L4.02154 12.9998L22 12.9998C22.5523 12.9998 23 12.5521 23 11.9998C23 11.4476 22.5523 10.9998 22 10.9998L4.01675 10.9998L7.68473 7.33186Z" fill="#fff"/>
					</svg>
				</a>
				<h2 class="drawer__h2">Basket of goods</h2>
			</div>

			<div class="drawer__list">

				<div class="drawer__item">
					<button class="drawer__close">
						<svg width="24px" height="24px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M19.207 6.207a1 1 0 0 0-1.414-1.414L12 10.586 6.207 4.793a1 1 0 0 0-1.414 1.414L10.586 12l-5.793 5.793a1 1 0 1 0 1.414 1.414L12 13.414l5.793 5.793a1 1 0 0 0 1.414-1.414L13.414 12l5.793-5.793z" fill="#fff"/></svg>
					</button>
					<img src="../assets/img/cards1.jpg" class="drawer__img" alt="">
					<div class="drawer__item_content">
						<p class="cards__item_name">Adidas top</p>
						<p class="cards__item_brand">Adidas</p>
						<p class="cards__item_text">A very stylish option for morning runs...</p>
						<div class="drawer__item_price">
							<span class="cards__item_price--old">123123 $</span>
							<span class="cards__item_price--sale">123123 $</span>
						</div>
					</div>
				</div>

				<div class="drawer__item">
					<button class="drawer__close">
						<svg width="24px" height="24px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M19.207 6.207a1 1 0 0 0-1.414-1.414L12 10.586 6.207 4.793a1 1 0 0 0-1.414 1.414L10.586 12l-5.793 5.793a1 1 0 1 0 1.414 1.414L12 13.414l5.793 5.793a1 1 0 0 0 1.414-1.414L13.414 12l5.793-5.793z" fill="#fff"/></svg>
					</button>
					<img src="../assets/img/cards1.jpg" class="drawer__img" alt="">
					<div class="drawer__item_content">
						<p class="cards__item_name">Adidas top</p>
						<p class="cards__item_brand">Adidas</p>
						<p class="cards__item_text">A very stylish option for morning runs...</p>
						<div class="drawer__item_price">
							<span class="cards__item_price--old">123123 $</span>
							<span class="cards__item_price--sale">123123 $</span>
						</div>
					</div>
				</div>

				<div class="drawer__item">
					<button class="drawer__close">
						<svg width="24px" height="24px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M19.207 6.207a1 1 0 0 0-1.414-1.414L12 10.586 6.207 4.793a1 1 0 0 0-1.414 1.414L10.586 12l-5.793 5.793a1 1 0 1 0 1.414 1.414L12 13.414l5.793 5.793a1 1 0 0 0 1.414-1.414L13.414 12l5.793-5.793z" fill="#fff"/></svg>
					</button>
					<img src="../assets/img/cards1.jpg" class="drawer__img" alt="">
					<div class="drawer__item_content">
						<p class="cards__item_name">Adidas top</p>
						<p class="cards__item_brand">Adidas</p>
						<p class="cards__item_text">A very stylish option for morning runs...</p>
						<div class="drawer__item_price">
							<span class="cards__item_price--old">123123 $</span>
							<span class="cards__item_price--sale">123123 $</span>
						</div>
					</div>
				</div>
				
				<div class="drawer__item">
					<button class="drawer__close">
						<svg width="24px" height="24px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M19.207 6.207a1 1 0 0 0-1.414-1.414L12 10.586 6.207 4.793a1 1 0 0 0-1.414 1.414L10.586 12l-5.793 5.793a1 1 0 1 0 1.414 1.414L12 13.414l5.793 5.793a1 1 0 0 0 1.414-1.414L13.414 12l5.793-5.793z" fill="#fff"/></svg>
					</button>
					<img src="../assets/img/cards1.jpg" class="drawer__img" alt="">
					<div class="drawer__item_content">
						<p class="cards__item_name">Adidas top</p>
						<p class="cards__item_brand">Adidas</p>
						<p class="cards__item_text">A very stylish option for morning runs...</p>
						<div class="drawer__item_price">
							<span class="cards__item_price--old">123123 $</span>
							<span class="cards__item_price--sale">123123 $</span>
						</div>
					</div>
				</div>

			</div>

			<div class="drawer__footer">
				<p><b>Total price: 123123</b></p>
				<button class="btn">Buy goods</button>
			</div>

		</div>
	</div>
</template>
