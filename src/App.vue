<script setup>
	import { onMounted, ref, watch } from "vue";
	import axios from 'axios';

	import Header from "./components/Header.vue";
	import Hero from "./components/Hero.vue";
	import CardList from "./components/CardList.vue";
	import Drawer from "./components/Drawer.vue";
	import Modal from "./components/Modal.vue";
	import Js from "./components/Js.vue";


</script>

<template>
	<div class="accent--red">
		<Header></Header>

		<Hero></Hero>

		<CardList ></CardList>

		<Drawer></Drawer>

		<!-- <div class="developments bg--dark">
			<div class="container">
				<p class="developments__title">Latest developments</p>

				<p class="developments__text">
					Everyday practice shows that constant quantitative growth and the
					scope of <br />
					our activity allows us to evaluate the significance of the development
					model.
				</p>

				<div class="developments__slider swiper-container">
					<div class="swiper-wrapper">
						<a
							href="#"
							class="developments__item developments--text_open swiper-slide"
						>
							<img src="../src/assets/img/developments1.jpg" alt="" />
							<div class="developments__item_description">
								<p class="developments__item_title">Order in 1 click</p>
								<p class="developments__item_text">
									Diverse and rich experience, constant quantitative growth
									and...
								</p>
							</div>
						</a>

						<a
							href="#"
							class="developments__item developments_open swiper-slide"
						>
							<img src="../src/assets/img/developments2.jpg" alt="" />
							<div class="developments__item_description">
								<p class="developments__item_title">We'll deliver today</p>
								<p class="developments__item_text">
									We deliver goods all over the world
								</p>
							</div>
						</a>

						<a
							href="#"
							class="developments__item developments_open swiper-slide"
						>
							<img src="../src/assets/img/developments3.jpg" alt="" />
							<div class="developments__item_description">
								<p class="developments__item_title">
									We'll refund your money if it doesn't suit you
								</p>
								<p class="developments__item_text">
									We deliver goods all over the world
								</p>
							</div>
						</a>

						<a
							href="#"
							class="developments__item developments_open swiper-slide"
						>
							<img src="../src/assets/img/developments2.jpg" alt="" />
							<div class="developments__item_description">
								<p class="developments__item_title">Order in 1 click</p>
								<p class="developments__item_text">
									Diverse and rich experience, constant quantitative growth
									and...
								</p>
							</div>
						</a>

						<a
							href="#"
							class="developments__item developments_open swiper-slide"
						>
							<img src="../src/assets/img/developments2.jpg" alt="" />
							<div class="developments__item_description">
								<p class="developments__item_title">We'll deliver today</p>
								<p class="developments__item_text">
									We deliver goods all over the world
								</p>
							</div>
						</a>

						<a
							href="#"
							class="developments__item developments_open swiper-slide"
						>
							<img src="../src/assets/img/developments3.jpg" alt="" />
							<div class="developments__item_description">
								<p class="developments__item_title">
									We'll refund your money if it doesn't suit you
								</p>
								<p class="developments__item_text">
									We deliver goods all over the world
								</p>
							</div>
						</a>

						<a
							href="#"
							class="developments__item developments_open swiper-slide"
						>
							<img src="../src/assets/img/developments2.jpg" alt="" />
							<div class="developments__item_description">
								<p class="developments__item_title">Order in 1 click</p>
								<p class="developments__item_text">
									Diverse and rich experience, constant quantitative growth
									and...
								</p>
							</div>
						</a>
					</div>
				</div>

				<div class="developments__nav">
					<div class="developments__nav_pagination swiper-pagination"></div>
				</div>
			</div>
		</div>

		<div class="reviews bg--light">
			<div class="container">
				<p class="reviews__title">Reviews from our customers</p>
				<p class="reviews__text">
					Everyday practice shows that constant quantitative growth and the
					scope of our activity allows evaluate the significance of the
					development model. On the other hand, constant information and
					propaganda support our activity plays an important role in the
					formation of new proposals.
					<br />
					<a href="#">
						<svg
							width="24"
							height="24"
							viewBox="0 0 24 24"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M9 22C8.73478 22 8.48043 21.8946 8.29289 21.7071C8.10536 21.5196 8 21.2652 8 21V18H4C3.46957 18 2.96086 17.7893 2.58579 17.4142C2.21071 17.0391 2 16.5304 2 16V4C2 2.89 2.9 2 4 2H20C20.5304 2 21.0391 2.21071 21.4142 2.58579C21.7893 2.96086 22 3.46957 22 4V16C22 16.5304 21.7893 17.0391 21.4142 17.4142C21.0391 17.7893 20.5304 18 20 18H13.9L10.2 21.71C10 21.9 9.75 22 9.5 22H9ZM10 16V19.08L13.08 16H20V4H4V16H10ZM11 6H13V9H16V11H13V14H11V11H8V9H11V6Z"
								fill="#D32F2F"
							/>
						</svg>
						Leave feedback
					</a>
				</p>

				<div class="reviews__slider swiper-container">
					<div class="swiper-wrapper">
						<div class="reviews__item swiper-slide">
							<p class="reviews__item_text">
								Thus, strengthening and developing the structure requires us to
								analyze the forms of development. Likewise, the existing
								structure of the organization requires us to analyze the
								appropriate activation conditions. Thus the beginning of the
								daily...
							</p>
							<div class="reviews__item_info">
								<p class="reviews__item_name">Ivanov Yuri V.</p>
								<p class="reviews__item_place">England London</p>
							</div>
						</div>

						<div class="reviews__item swiper-slide">
							<p class="reviews__item_text">
								Diverse and rich experience constant quantitative growth and
								scope of our activity contributes to the preparation and
								implementation of areas of progressive development. The task of
								the organization especially the existing structure of the
								organization...
							</p>
							<div class="reviews__item_info">
								<img src="../src/assets/img/avatar1.png" alt="" />
								<p class="reviews__item_name">Demidov Valery I.</p>
								<p class="reviews__item_place">England London</p>
							</div>
						</div>

						<div class="reviews__item swiper-slide">
							<p class="reviews__item_text">
								In general, excellent service, delivery is almost instant and
								straight into your hands. At the same time, I also took 2
								additional sizes to choose from. The courier, sweetie, waited
								patiently and advised. Thank you!!!
							</p>
							<div class="reviews__item_info">
								<img src="../src/assets/img/avatar2.png" alt="" />
								<p class="reviews__item_name">Smirnova Vasilisa V.</p>
								<p class="reviews__item_place">USA, Washington</p>
							</div>
						</div>

						<div class="reviews__item swiper-slide">
							<p class="reviews__item_text">
								In general, excellent service, delivery is almost instant and
								straight into your hands. At the same time, I also took 2
								additional sizes to choose from. The courier, sweetie, waited
								patiently and advised. Thank you!!!
							</p>
							<div class="reviews__item_info">
								<img src="../src/assets/img/avatar2.png" alt="" />
								<p class="reviews__item_name">Smirnova Vasilisa V.</p>
								<p class="reviews__item_place">USA, Washington</p>
							</div>
						</div>
					</div>
				</div>

				<div class="reviews__nav">
					<div class="reviews__nav_button reviews__nav_prev">
						<span></span> Previous
					</div>
					<div class="reviews__nav_button reviews__nav_next">
						Next <span></span>
					</div>
				</div>
			</div>
		</div>

		<div class="subscription bg--light">
			<div class="subscription__container container">
				<div class="subscription__description">
					<p class="subscription__title">Sign up to our newsletter</p>
					<p class="subscription__text">
						Everyday practice shows that constant quantitative <br />
						The growth and scope of our activity allows us to evaluate...
					</p>
				</div>

				<form class="subscription__form">
					<label for="email">Youre-mail:</label>
					<div class="subscription__form_line">
						<input type="email" placeholder="Email" id="email" required />
						<button type="submit">
							<svg
								width="16"
								height="16"
								viewBox="0 0 16 16"
								xmlns="http://www.w3.org/2000/svg"
							>
								<g>
									<path
										d="M15.843 0.136458C15.7004 0.00219689 15.4934 -0.0363783 15.3142 0.0358625L0.314413 6.03578C0.14889 6.10218 0.0316953 6.25063 0.00534393 6.42688C-0.0205398 6.60265 0.0487952 6.7794 0.187465 6.89025L4.99991 10.742V13.5C4.99991 13.6845 5.10147 13.854 5.26405 13.9409C5.3378 13.9805 5.41882 14 5.49988 14C5.59704 14 5.69372 13.9717 5.77722 13.916L7.2355 12.9438L10.1463 15.8535C10.241 15.9482 10.3689 16 10.4998 16C10.5379 16 10.5764 15.9956 10.6145 15.9868C10.7835 15.9467 10.9192 15.8222 10.9739 15.6582L15.9739 0.658442C16.0359 0.473849 15.9846 0.270252 15.843 0.136458ZM13.4238 1.86917L5.46181 9.83114L1.48189 6.64564L13.4238 1.86917ZM5.99989 12.566V11.7088L6.51429 12.2229L5.99989 12.566ZM10.2811 14.5747L6.20599 10.501L14.3555 2.35154L10.2811 14.5747Z"
										fill="white"
									/>
								</g>
								<defs>
									<clipPath id="clip0">
										<rect width="16" height="16" fill="white" />
									</clipPath>
								</defs>
							</svg>
						</button>
					</div>
					<p class="policy">
						<svg
							width="16"
							height="16"
							viewBox="0 0 16 16"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M8 0C3.6 0 0 3.6 0 8C0 12.4 3.6 16 8 16C12.4 16 16 12.4 16 8C16 3.6 12.4 0 8 0ZM6.4 12L2.4 8L3.528 6.872L6.4 9.736L12.472 3.664L13.6 4.8L6.4 12Z"
								fill="#D32F2F"
							/>
						</svg>
						I agree with the terms of
						<a href="#" target=" _blank">processing of personal data</a>
					</p>
				</form>
			</div>
		</div>

		<div class="gallery">
			<div class="container">
				<h2>See how you can use our products</h2>
				<p class="gallery__text">
					Daily practice shows that constant quantitative growth and the scope
					of our activity allows you to evaluate the significance of the
					development model. On the other hand, constant information and
					propaganda ensuring our activities plays an important role in the
					formation of new proposals.
				</p>

				<div class="gallery__grid" id="gallery__grid">
					<a
						href="../src/assets/img/gallery2.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_50"
					>
						<img src="../src/assets/img/gallery1.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery2.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery2.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery3.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery3.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery4.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery4.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery5.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery5.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery6.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery6.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery7.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery7.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery8.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery8.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery9.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery9.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery4.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery4.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery5.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery5.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery6.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery6.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery7.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery7.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery8.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery8.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery9.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery9.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery4.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery4.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery5.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery5.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery6.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery6.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery7.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery7.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery8.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery8.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery9.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery9.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery4.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery4.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery5.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery5.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery6.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery6.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery7.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery7.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery8.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery8.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery9.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_12"
					>
						<img src="../src/assets/img/gallery9.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery2.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_50"
					>
						<img src="../src/assets/img/gallery1.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery2.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery2.jpg" alt="" />
					</a>
					<a
						href="../src/assets/img/gallery3.jpg"
						data-fancybox="gallery"
						class="gallery__item gallery__item_25"
					>
						<img src="../src/assets/img/gallery3.jpg" alt="" />
					</a>
				</div>

				<span class="click">
					<a href="#gallery__grid" class="gallery__more">
						<svg
							width="24"
							height="24"
							viewBox="0 0 24 24"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M19 11H15V15H13V11H9V9H13V5H15V9H19V11ZM20 2H8C7.46957 2 6.96086 2.21071 6.58579 2.58579C6.21071 2.96086 6 3.46957 6 4V16C6 16.5304 6.21071 17.0391 6.58579 17.4142C6.96086 17.7893 7.46957 18 8 18H20C20.5304 18 21.0391 17.7893 21.4142 17.4142C21.7893 17.0391 22 16.5304 22 16V4C22 3.46957 21.7893 2.96086 21.4142 2.58579C21.0391 2.21071 20.5304 2 20 2ZM4 6H2V20C2 20.5304 2.21071 21.0391 2.58579 21.4142C2.96086 21.7893 3.46957 22 4 22H18V20H4V6Z"
								fill="#D32F2F"
							/>
						</svg>
						<span>More photos</span>
					</a>
				</span>
			</div>
		</div>

		<div class="certified reviews bg--light">
			<div class="container">
				<p class="reviews__title">All products are certified</p>
				<p class="reviews__text">
					Everyday practice shows that constant quantitative growth and the
					scope of our activity allows evaluate the significance of the
					development model. On the other hand, constant information and
					propaganda support our activity plays an important role in the
					formation of new proposals.
				</p>

				<div class="certified__slider swiper-container">
					<div class="swiper-wrapper">
						<div class="certified__item swiper-slide">
							<div class="certified__item_img">
								<img src="../src/assets/img/certified1.jpg" alt="" />
							</div>
							<p class="certified__item_title">
								Name of the certificate with additional annexes and other
								related documents
							</p>
							<a href="#" class="certified__item_download">PDF, 2.2 Mb</a>
						</div>

						<div class="certified__item swiper-slide">
							<div class="certified__item_img">
								<img src="../src/assets/img/certified1.jpg" alt="" />
							</div>
							<p class="certified__item_title">
								Name of the certificate with additional annexes and other
								related documents
							</p>
							<a href="#" class="certified__item_download">PDF, 2.2 Mb</a>
						</div>

						<div class="certified__item swiper-slide">
							<div class="certified__item_img">
								<img src="../src/assets/img/certified1.jpg" alt="" />
							</div>
							<p class="certified__item_title">
								Name of the certificate with additional annexes and other
								related documents
							</p>
							<a href="#" class="certified__item_download">PDF, 2.2 Mb</a>
						</div>

						<div class="certified__item swiper-slide">
							<div class="certified__item_img">
								<img src="../src/assets/img/certified1.jpg" alt="" />
							</div>
							<p class="certified__item_title">
								Name of the certificate with additional annexes and other
								related documents
							</p>
							<a href="#" class="certified__item_download">PDF, 2.2 Mb</a>
						</div>
					</div>
				</div>

				<div class="certified__nav">
					<div class="certified__nav_button certified__nav_prev">
						<span></span> Previous
					</div>
					<div class="certified__nav_button certified__nav_next">
						Next <span></span>
					</div>
				</div>
			</div>
		</div>

		<div class="doubt">
			<div class="container">
				<p class="doubt__title">Any doubts left? We will dispel them!</p>
				<p class="doubt__text">
					Everyday practice shows that constant quantitative growth and the
					scope of our activity <br />
					allows us to evaluate the significance of the development model.
				</p>

				<div class="doubt__content">
					<div class="doubt__list">
						<div class="doubt__list_item">
							<p class="doubt__list_number">
								<svg
									width="32"
									height="32"
									viewBox="0 0 32 32"
									fill="none"
									xmlns="http://www.w3.org/2000/svg"
								>
									<circle
										cx="16"
										cy="16"
										r="13"
										stroke="#D32F2F"
										stroke-width="6"
									/>
								</svg>
								<span>1</span>
							</p>
							<p class="doubt__list_title">
								A long formulation of an interesting question, about everything
								that exists?
							</p>
							<p class="doubt__list_text">
								Daily practice shows that constant quantitative growth and the
								scope of our activity allows us to evaluate the significance of
								the development model.
							</p>
						</div>
						<div class="doubt__list_item">
							<p class="doubt__list_number">
								<svg
									width="32"
									height="32"
									viewBox="0 0 32 32"
									fill="none"
									xmlns="http://www.w3.org/2000/svg"
								>
									<circle
										cx="16"
										cy="16"
										r="13"
										stroke="#D32F2F"
										stroke-width="6"
									/>
								</svg>
								<span>2</span>
							</p>
							<p class="doubt__list_title">
								A long formulation of an interesting question, about everything
								that exists?
							</p>
							<p class="doubt__list_text">
								Daily practice shows that constant quantitative growth and the
								scope of our activity allows us to evaluate the significance of
								the development model.
							</p>
						</div>
						<div class="doubt__list_item">
							<p class="doubt__list_number">
								<svg
									width="32"
									height="32"
									viewBox="0 0 32 32"
									fill="none"
									xmlns="http://www.w3.org/2000/svg"
								>
									<circle
										cx="16"
										cy="16"
										r="13"
										stroke="#D32F2F"
										stroke-width="6"
									/>
								</svg>
								<span>3</span>
							</p>
							<p class="doubt__list_title">
								A long formulation of an interesting question, about everything
								that exists?
							</p>
							<p class="doubt__list_text">
								Daily practice shows that constant quantitative growth and the
								scope of our activity allows us to evaluate the significance of
								the development model.
							</p>
						</div>
						<div class="doubt__list_item">
							<p class="doubt__list_number">
								<svg
									width="32"
									height="32"
									viewBox="0 0 32 32"
									fill="none"
									xmlns="http://www.w3.org/2000/svg"
								>
									<circle
										cx="16"
										cy="16"
										r="13"
										stroke="#D32F2F"
										stroke-width="6"
									/>
								</svg>
								<span>4</span>
							</p>
							<p class="doubt__list_title">
								A long formulation of an interesting question, about everything
								that exists?
							</p>
							<p class="doubt__list_text">
								Daily practice shows that constant quantitative growth and the
								scope of our activity allows us to evaluate the significance of
								the development model.
							</p>
						</div>
					</div>

					<div class="doubt__download">
						<div class="doubt__download_img">
							<img src="../src/assets/img/doubt.jpg" alt="" />
						</div>
						<p class="doubt__download_title">
							The name of the instructions or manual for using the product or
							categories of products produced by our company.
						</p>
						<p><a href="#" class="doubt__download_link">PDF, 25.2 Mb</a></p>
						<p>
							<a href="#" class="doubt__download_down">
								<svg
									width="24"
									height="24"
									viewBox="0 0 24 24"
									xmlns="http://www.w3.org/2000/svg"
								>
									<path
										d="M5 20H19V18H5V20ZM19 9H15V3H9V9H5L12 16L19 9Z"
										fill="#D32F2F"
									/>
								</svg>
								Download full instructions
							</a>
						</p>
					</div>
				</div>
			</div>
		</div>

		<div class="about bg--light" id="about">
			<div class="container">
				<p class="about__title">About our company</p>

				<div class="about__content">
					<div class="about__img">
						<img src="../src/assets/img/about1.png" alt="" />
					</div>
					<div class="about__text">
						<p>
							Comrades! the new model of organizational activity largely
							determines creation of a personnel training system that meets
							urgent needs. Equally constant information and propaganda support
							of our activities require us analysis of the corresponding
							activation conditions. Thus, the new model of organizational
							activities ensures a wide range (specialists) participation in the
							formation of appropriate activation conditions. Everyday practice
							shows that the scope and location of personnel training plays a
							role important role in shaping the development model.
						</p>
						<p>
							Thus, the implementation of the planned targets is an interesting
							experiment. checking the personnel training system meets urgent
							needs. It should not be forgotten, however, that the strengthening
							and development of the structure contributes to the preparation
							and implementation of forms of development.
						</p>
						<p>
							Thus, consultation with a wide range of assets largely determines
							the creation personnel training system meets urgent needs. On the
							other hand, the current the structure of the organization entails
							a process of implementation and modernization corresponding to the
							conditions activation.
							<br />
							However, one should not forget that the existing structure of the
							organization requires defining and clarifying the positions taken
							by participants regarding...
						</p>
						<div class="about__text_none">
							<p>
								Comrades! the new model of organizational activity largely
								determines creation of a personnel training system that meets
								urgent needs. Equally constant information and propaganda
								support of our activities require us analysis of the
								corresponding activation conditions. Thus, the new model of
								organizational activities ensures a wide range (specialists)
								participation in the formation of appropriate activation
								conditions. Everyday practice shows that the scope and location
								of personnel training plays a role important role in shaping the
								development model.
							</p>
							<p>
								Thus, the implementation of the planned targets is an
								interesting experiment. checking the personnel training system
								meets urgent needs. It should not be forgotten, however, that
								the strengthening and development of the structure contributes
								to the preparation and implementation of forms of development.
							</p>
							<p>
								Thus, consultation with a wide range of assets largely
								determines the creation personnel training system meets urgent
								needs. On the other hand, the current the structure of the
								organization entails a process of implementation and
								modernization corresponding to the conditions activation.
								<br />
								However, one should not forget that the existing structure of
								the organization requires defining and clarifying the positions
								taken by participants regarding...
							</p>
						</div>
						<span class="about__text_more">
							<svg
								width="24"
								height="24"
								viewBox="0 0 24 24"
								xmlns="http://www.w3.org/2000/svg"
							>
								<path
									d="M21 6V8H3V6H21ZM3 18H12V16H3V18ZM3 13H21V11H3V13Z"
									fill="#D32F2F"
								/>
							</svg>
							<span>Read completely</span>
						</span>
						<a href="#" class="about__info">
							<img src="../src/assets/img/about__info.svg" alt="" />
							<div>
								<p class="about__info_title">Company details</p>
								<p class="about__info_text">
									Everyday practice shows that constant quantitative growth and
									the scope of our activity allows you to evaluate...
								</p>
							</div>
						</a>
					</div>
				</div>
			</div>
		</div>

		<div class="video">
			<div class="container">
				<p class="video__title">Watch the video About our company!</p>

				<div class="video__slider swiper-container">
					<div class="swiper-wrapper">
						<div class="swiper-slide">
							<iframe
								width="1663"
								height="738"
								src="https://www.youtube.com/embed/G7LEmT21dLw"
								frameborder="0"
								allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
								allowfullscreen
							></iframe>
						</div>
						<div class="swiper-slide">
							<iframe
								width="1663"
								height="738"
								src="https://www.youtube.com/embed/G7LEmT21dLw"
								frameborder="0"
								allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
								allowfullscreen
							></iframe>
						</div>
						<div class="swiper-slide">
							<iframe
								width="1663"
								height="738"
								src="https://www.youtube.com/embed/G7LEmT21dLw"
								frameborder="0"
								allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
								allowfullscreen
							></iframe>
						</div>
					</div>
					<div class="video__pagination swiper-pagination"></div>
					<div class="video__button">
						<div class="video__button_prev"></div>
						<div class="video__button_next"></div>
					</div>
				</div>
			</div>
		</div>

		<div class="contacts bg--light" id="contacts">
			<div class="container">
				<h2 class="contacts__title">Contacts</h2>

				<div class="contacts__list">
					<div class="contacts__item">
						<span>Phones</span>
						<div>
							<img src="../src/assets/img/contacts__tel.svg" alt="" />
							<p>
								<a href="tel:+78001234567">+3 800 123-45-67</a>
								<a href="tel:+74951556677">+3 495 155-66-77</a>
							</p>
						</div>
					</div>
					<div class="contacts__item">
						<span>Mail</span>
						<div>
							<img src="../src/assets/img/contacts__mail.svg" alt="" />
							<p>
								<a href="mailto:info@company.ru">info@company.ru</a>
							</p>
						</div>
					</div>
					<div class="contacts__item">
						<span>Working hours</span>
						<div>
							<img src="../src/assets/img/contacts__time.svg" alt="" />
							<p>Mon. - Fri. : <br />from 9:00 to 18:00</p>
						</div>
					</div>
					<div class="contacts__item">
						<span>Company address</span>
						<div>
							<img src="../src/assets/img/contacts__place.svg" alt="" />
							<p>
								g. Washington, <br />
								st. Josh, 15
							</p>
						</div>
					</div>
				</div>

				<div class="contacts__map">
					<iframe
						src="https://www.google.com/maps/d/embed?mid=1NhRcCG7FNJMzqcM5yZEdsFX5OMY&hl=ru&ehbc=2E312F"
						width="640"
						height="480"
					></iframe>
				</div>
			</div>
		</div>

		<div class="question">
			<div class="container">
				<p class="question__title">
					Still have questions? We will be happy to help!
				</p>
				<p class="question__text">
					Everyday practice shows that constant quantitative growth and scope
					our activity allows you to evaluate...
				</p>

				<form class="question__form" method="post">
					<div class="question__form_line">
						<label for="name">Your name</label>
						<input type="text" name="name" id="name" placeholder="Your name" />
					</div>
					<div class="question__form_line">
						<label for="tel">Contact number</label>
						<input
							type="tel"
							name="tel"
							id="tel"
							placeholder="Contact number"
						/>
					</div>
					<div class="question__form_btn">
						<button class="btn">Send</button>
					</div>
					<p class="policy">
						<svg
							width="16"
							height="16"
							viewBox="0 0 16 16"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M8 0C3.6 0 0 3.6 0 8C0 12.4 3.6 16 8 16C12.4 16 16 12.4 16 8C16 3.6 12.4 0 8 0ZM6.4 12L2.4 8L3.528 6.872L6.4 9.736L12.472 3.664L13.6 4.8L6.4 12Z"
								fill="#D32F2F"
							/>
						</svg>
						I agree with the terms of
						<a href="#" target=" _blank">processing of personal data</a>
					</p>
				</form>
			</div>
		</div>

		<footer class="footer">
			<div class="footer__info container">
				<a href="#" class="footer__logo">Logotype</a>
				<div class="footer__soc">
					<a href="#" target="_blank">
						<svg
							width="24"
							height="24"
							viewBox="0 0 24 24"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M15.07 2H8.93C3.33 2 2 3.33 2 8.93V15.07C2 20.67 3.33 22 8.93 22H15.07C20.67 22 22 20.67 22 15.07V8.93C22 3.33 20.67 2 15.07 2ZM18.15 16.27H16.69C16.14 16.27 15.97 15.82 15 14.83C14.12 14 13.74 13.88 13.53 13.88C13.24 13.88 13.15 13.96 13.15 14.38V15.69C13.15 16.04 13.04 16.26 12.11 16.26C10.57 16.26 8.86 15.32 7.66 13.59C5.85 11.05 5.36 9.13 5.36 8.75C5.36 8.54 5.43 8.34 5.85 8.34H7.32C7.69 8.34 7.83 8.5 7.97 8.9C8.69 11 9.89 12.8 10.38 12.8C10.57 12.8 10.65 12.71 10.65 12.25V10.1C10.6 9.12 10.07 9.03 10.07 8.68C10.07 8.5 10.21 8.34 10.44 8.34H12.73C13.04 8.34 13.15 8.5 13.15 8.88V11.77C13.15 12.08 13.28 12.19 13.38 12.19C13.56 12.19 13.72 12.08 14.05 11.74C15.1 10.57 15.85 8.76 15.85 8.76C15.95 8.55 16.11 8.35 16.5 8.35H17.93C18.37 8.35 18.47 8.58 18.37 8.89C18.19 9.74 16.41 12.25 16.43 12.25C16.27 12.5 16.21 12.61 16.43 12.9C16.58 13.11 17.09 13.55 17.43 13.94C18.05 14.65 18.53 15.24 18.66 15.65C18.77 16.06 18.57 16.27 18.15 16.27Z"
							/>
						</svg>
					</a>
					<a href="#" target="_blank">
						<svg
							width="24"
							height="24"
							viewBox="0 0 24 24"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M12 2.04004C6.5 2.04004 2 6.53004 2 12.06C2 17.06 5.66 21.21 10.44 21.96V14.96H7.9V12.06H10.44V9.85004C10.44 7.34004 11.93 5.96004 14.22 5.96004C15.31 5.96004 16.45 6.15004 16.45 6.15004V8.62004H15.19C13.95 8.62004 13.56 9.39004 13.56 10.18V12.06H16.34L15.89 14.96H13.56V21.96C15.9164 21.5879 18.0622 20.3856 19.6099 18.5701C21.1576 16.7546 22.0054 14.4457 22 12.06C22 6.53004 17.5 2.04004 12 2.04004Z"
								fill="#9D9D9D"
							/>
						</svg>
					</a>
					<a href="#" target="_blank">
						<svg
							width="24"
							height="24"
							viewBox="0 0 24 24"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M10 15L15.19 12L10 9V15ZM21.56 7.17C21.69 7.64 21.78 8.27 21.84 9.07C21.91 9.87 21.94 10.56 21.94 11.16L22 12C22 14.19 21.84 15.8 21.56 16.83C21.31 17.73 20.73 18.31 19.83 18.56C19.36 18.69 18.5 18.78 17.18 18.84C15.88 18.91 14.69 18.94 13.59 18.94L12 19C7.81 19 5.2 18.84 4.17 18.56C3.27 18.31 2.69 17.73 2.44 16.83C2.31 16.36 2.22 15.73 2.16 14.93C2.09 14.13 2.06 13.44 2.06 12.84L2 12C2 9.81 2.16 8.2 2.44 7.17C2.69 6.27 3.27 5.69 4.17 5.44C4.64 5.31 5.5 5.22 6.82 5.16C8.12 5.09 9.31 5.06 10.41 5.06L12 5C16.19 5 18.8 5.16 19.83 5.44C20.73 5.69 21.31 6.27 21.56 7.17Z"
								fill="#9D9D9D"
							/>
						</svg>
					</a>
					<a href="#" target="_blank">
						<svg
							width="24"
							height="24"
							viewBox="0 0 24 24"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M17.8301 12.74C17.5501 12.17 16.7601 11.69 15.7101 12.5C14.2801 13.64 12.0001 13.64 12.0001 13.64C12.0001 13.64 9.72005 13.64 8.29005 12.5C7.24005 11.69 6.45005 12.17 6.17005 12.74C5.67005 13.74 6.23005 14.23 7.50005 15.04C8.59005 15.74 10.0801 16 11.0401 16.1L10.2401 16.9C9.10005 18.03 8.00005 19.12 7.25005 19.88C6.80005 20.34 6.80005 21.07 7.25005 21.5L7.39005 21.66C7.84005 22.11 8.58005 22.11 9.03005 21.66L12.0001 18.68C13.1501 19.81 14.2401 20.9 15.0001 21.66C15.4501 22.11 16.18 22.11 16.64 21.66L16.7701 21.5C17.2301 21.07 17.2301 20.34 16.7701 19.88L13.7901 16.9L13.0001 16.09C13.9501 16 15.4201 15.73 16.5001 15.04C17.7701 14.23 18.3301 13.74 17.8301 12.74ZM12.0001 4.57C13.3801 4.57 14.5001 5.69 14.5001 7.06C14.5001 8.44 13.3801 9.55 12.0001 9.55C10.6201 9.55 9.50005 8.44 9.50005 7.06C9.50005 5.69 10.6201 4.57 12.0001 4.57ZM12.0001 12.12C14.8001 12.12 17.0601 9.86 17.0601 7.06C17.0601 4.27 14.8001 2 12.0001 2C9.20005 2 6.94005 4.27 6.94005 7.06C6.94005 9.86 9.20005 12.12 12.0001 12.12Z"
								fill="#9D9D9D"
							/>
						</svg>
					</a>
					<a href="#" target="_blank">
						<svg
							width="24"
							height="24"
							viewBox="0 0 24 24"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M22.46 6C21.69 6.35 20.86 6.58 20 6.69C20.88 6.16 21.56 5.32 21.88 4.31C21.05 4.81 20.13 5.16 19.16 5.36C18.37 4.5 17.26 4 16 4C13.65 4 11.73 5.92 11.73 8.29C11.73 8.63 11.77 8.96 11.84 9.27C8.28004 9.09 5.11004 7.38 3.00004 4.79C2.63004 5.42 2.42004 6.16 2.42004 6.94C2.42004 8.43 3.17004 9.75 4.33004 10.5C3.62004 10.5 2.96004 10.3 2.38004 10C2.38004 10 2.38004 10 2.38004 10.03C2.38004 12.11 3.86004 13.85 5.82004 14.24C5.46004 14.34 5.08004 14.39 4.69004 14.39C4.42004 14.39 4.15004 14.36 3.89004 14.31C4.43004 16 6.00004 17.26 7.89004 17.29C6.43004 18.45 4.58004 19.13 2.56004 19.13C2.22004 19.13 1.88004 19.11 1.54004 19.07C3.44004 20.29 5.70004 21 8.12004 21C16 21 20.33 14.46 20.33 8.79C20.33 8.6 20.33 8.42 20.32 8.23C21.16 7.63 21.88 6.87 22.46 6Z"
								fill="#9D9D9D"
							/>
						</svg>
					</a>
					<a href="#" target="_blank">
						<svg
							width="24"
							height="24"
							viewBox="0 0 24 24"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M7.8 2H16.2C19.4 2 22 4.6 22 7.8V16.2C22 17.7383 21.3889 19.2135 20.3012 20.3012C19.2135 21.3889 17.7383 22 16.2 22H7.8C4.6 22 2 19.4 2 16.2V7.8C2 6.26174 2.61107 4.78649 3.69878 3.69878C4.78649 2.61107 6.26174 2 7.8 2ZM7.6 4C6.64522 4 5.72955 4.37928 5.05442 5.05442C4.37928 5.72955 4 6.64522 4 7.6V16.4C4 18.39 5.61 20 7.6 20H16.4C17.3548 20 18.2705 19.6207 18.9456 18.9456C19.6207 18.2705 20 17.3548 20 16.4V7.6C20 5.61 18.39 4 16.4 4H7.6ZM17.25 5.5C17.5815 5.5 17.8995 5.6317 18.1339 5.86612C18.3683 6.10054 18.5 6.41848 18.5 6.75C18.5 7.08152 18.3683 7.39946 18.1339 7.63388C17.8995 7.8683 17.5815 8 17.25 8C16.9185 8 16.6005 7.8683 16.3661 7.63388C16.1317 7.39946 16 7.08152 16 6.75C16 6.41848 16.1317 6.10054 16.3661 5.86612C16.6005 5.6317 16.9185 5.5 17.25 5.5ZM12 7C13.3261 7 14.5979 7.52678 15.5355 8.46447C16.4732 9.40215 17 10.6739 17 12C17 13.3261 16.4732 14.5979 15.5355 15.5355C14.5979 16.4732 13.3261 17 12 17C10.6739 17 9.40215 16.4732 8.46447 15.5355C7.52678 14.5979 7 13.3261 7 12C7 10.6739 7.52678 9.40215 8.46447 8.46447C9.40215 7.52678 10.6739 7 12 7ZM12 9C11.2044 9 10.4413 9.31607 9.87868 9.87868C9.31607 10.4413 9 11.2044 9 12C9 12.7956 9.31607 13.5587 9.87868 14.1213C10.4413 14.6839 11.2044 15 12 15C12.7956 15 13.5587 14.6839 14.1213 14.1213C14.6839 13.5587 15 12.7956 15 12C15 11.2044 14.6839 10.4413 14.1213 9.87868C13.5587 9.31607 12.7956 9 12 9Z"
								fill="#9D9D9D"
							/>
						</svg>
					</a>
				</div>
				<div class="footer__info_info">
					<p>
						<a href="tel:+78001234567" class="">+3 800 123-45-67</a>
						<span>Mon. - Fri. from 9:00 to 21:00</span>
					</p>
					<a href="#" class="header__info_btn">
						<svg
							width="16"
							height="16"
							viewBox="0 0 16 16"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M15.1111 11.1111C14.0045 11.1111 12.9333 10.9333 11.9378 10.6045C11.6311 10.5067 11.28 10.5778 11.0356 10.8223L9.08004 12.7822C6.56004 11.5022 4.50225 9.44446 3.22225 6.92892L5.17779 4.96446C5.42225 4.72 5.49333 4.36892 5.39558 4.06225C5.06671 3.06671 4.88892 1.99558 4.88892 0.888917C4.88888 0.395542 4.49333 0 4 0H0.888875C0.4 0 0 0.395542 0 0.888875C0 9.23554 6.76446 16 15.1111 16C15.6045 16 16 15.6045 16 15.1111V12C16 11.5067 15.6045 11.1111 15.1111 11.1111Z"
								fill="white"
							/>
						</svg>
					</a>
				</div>
			</div>

			<div class="footer__copy container">
				<p>© 2001 - 2024. All rights reserved</p>
				<p><a href="#" target="_blank">Personal data processing policy</a></p>
				<p>
					<img src="../src/assets/img/footer1.png" alt="" />
					<img src="../src/assets/img/footer2.png" alt="" />
					<img src="../src/assets/img/footer3.png" alt="" />
					<img src="../src/assets/img/footer4.png" alt="" />
					<img src="../src/assets/img/footer5.png" alt="" />
				</p>
			</div>
		</footer> -->

		<!-- <Modal></Modal> -->
	</div>
</template>

<style scoped></style>
