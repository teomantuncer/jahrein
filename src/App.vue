<script>
export default {
	name: 'App',
	data() {
		return {
			history: [
				{
					year: 1988,
					title: '29 Kasım, Doğum, İstanbul',
					content: 'Bu iki güzel insanın çabaları sonucu, istenmeden dünyaya geliyor.',
					images: [
						'./timeline/ana-baba.jpg',
					]
				},
				{
					year: 1990,
					title: '2. yaş, Karabük',
					images: [
						'./timeline/2-yas.jpg',
					]
				},
				{
					year: 1993,
					title: '5. yaş, Karabük',
					images: [
						'./timeline/5-yas.jpg',
					]
				},
				{
					year: 1994,
					title: '6. yaş, İlkokul, Karabük',
				},
				{
					year: 2002,
					title: '13. yaş',
					images: [
						'./timeline/13-yas.jpg',
					]
				},
				{
					year: 2004,
					title: '15. yaş, Antalya Anadolu Lisesi',
					images: [
						'./timeline/15-yas.jpg',
					]
				},
				{
					year: 2005,
					title: '16. yaş, Antalya Anadolu Lisesi',
					images: [
						'./timeline/16-yas.jpg',
					]
				},
				{
					year: 2006,
					title: '17. yaş',
					images: [
						'./timeline/14-yas.jpg',
					]
				},
				{
					year: 2007,
					title: '18. yaş, Leipzig Üniversitesi, Almanya',
					images: [
						'./timeline/18-yas.jpg',
					]
				},
				{
					year: 2008,
					title: '19. yaş, Almanya',
					images: [
						'./timeline/19-yas.jpg',
					]
				},
				{
					year: 2009,
					title: '20. yaş, Almanya',
					images: [
						'./timeline/20-yas.png',
					]
				},
				{
					year: 2010,
					title: '21. yaş, Almanya',
					images: [
						'./timeline/21-yas.png',
					]
				},
				{
					year: 2011,
					title: '22. yaş, KKTC',
					images: [
						'./timeline/22-yas.jpg',
					]
				},
				{
					year: 2012,
					title: '23. yaş',
					images: [
						'./timeline/23-yas.jpg',
					]
				},
				{
					year: 2014,
					title: '25. yaş',
					images: [
						'./timeline/25-yas.jpg',
					]
				},
				{
					year: 2015,
					title: '26. yaş',
					images: [
						'./timeline/26-yas.jpg',
					]
				},
				{
					year: 2016,
					title: '27. yaş, Polonya',
					images: [
						'./timeline/27-yas.jpg',
					]
				},
				{
					year: 2017,
					title: '28. yaş',
					images: [
						'./timeline/28-yas.jpg',
					]
				},
				{
					year: 2018,
					title: '29. yaş',
					images: [
						'./timeline/29-yas.jpg',
					]
				},
				{
					year: 2019,
					title: '30. yaş, 5 Ekim, Antalya',
					images: [
						'./timeline/30-yas.jpg',
					]
				},
				{
					year: 2020,
					title: '31. yaş, Antalya',
					images: [
						'./timeline/31-yas.jpg',
					]
				},
				{
					year: 2021,
					title: '32. yaş, Antalya',
					content: 'Alfred\'in kazası, çalkantılı yıl.',
					images: [
						'./timeline/32-yas.jpg',
					]
				},
				{
					year: 2022,
					title: '33. yaş',
					content: 'Ahmet ile Selin ebeveyn olacaklarını öğrendiler.',
					images: [
						'./timeline/33-yas.jpg',
					]
				},
				{
					year: 2023,
					title: '34. yaş',
					images: [
						'./timeline/34-yas.jpg',
					]
				},
			]
		}
	}
	}
</script>
<template>
	<div class="pages">
		<div class="page intro">
			<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 244.47 406.23">
				<g class="glow">
					<path d="m0,45.4v45.53h244.46v-45.53l-35.71,22.77s-20.61,13.37-22.59-6.45V20.92c0-.37-.31-.67-.68-.66-.17,0-.34.07-.46.19l-26.41,26.41s-12.09,11.3-20-1.78L122.87.44c-.13-.35-.51-.53-.86-.4-.19.07-.33.21-.4.4l-12.38,33.54s-9.12,28.14-20.62,15.46l-30.58-28.68c-.27-.25-.69-.24-.95.03-.12.13-.18.29-.18.46v28.19s2,29.73-14.27,21.4c.03,0-18.31-4.1-42.63-25.44Z" />
					<path d="m244.37,237.9V103.04h-119.31v41.49l-.21.34h67v100.51c-.08,36.42-29.58,65.92-66,66h0c-34.89-.11-63.7-27.29-65.84-62.11l-.12.2H6.89c2.88,51.87,33.43,79.53,33.43,79.53l87.6,77.23,67.44-62.82c53.62-40.38,49.01-105.51,49.01-105.51Z" />
					<polygon class="biyik" points="91.28 243.71 125.69 220.01 160.15 243.71 152.53 251.33 125.69 235.67 98.9 251.33 91.28 243.71" />
				</g>
			</svg>
		</div>
		<div class="page history">
			<div class="timeline">
				<div class="title">Zaman çizelgesi...</div>
				<div v-for="(item, index) in history" :key="index" class="container" :class="index % 2 ? 'right' : 'left'" :data-aos-offset="index * 400" :data-aos="index % 2 ? 'zoom-in-right' : 'zoom-in-left'">
					<div class="content">
						<h2 v-if="item.year">{{ item.year }}</h2>
						<h3 v-if="item.title">{{ item.title }}</h3>
						<p v-if="item.content">{{ item.content }}</p>
						<ul v-if="item.images && item.images.length > 0" class="photos">
							<li v-for="(image, imageIndex) in item.images" :key="`${index}__${imageIndex}`">
								<img :src="image">
							</li>
						</ul>
					</div>
				</div>
			</div>
		</div>
		<div class="page outro">
			<h1 class="title">
				Hoççağalın
			</h1>
			<img data-aos="zoom-in-up" data-aos-offset="9600" src="/kafa.png" alt="">
		</div>
	</div>
</template>
<style scoped>
svg {
	animation: parlama 2s infinite linear;
	fill: rgb(255, 255, 255);
	height: 50vh;
	width: 50vh;
	border-radius: 50%;
	border: 1rem solid #fff;
	padding: 1rem;
	max-width: 50vw;
	max-height: 50vw;
}

@keyframes parlama {
	0% {
		filter: drop-shadow(0 0 20px rgba(255, 255, 255, 0.4))
	}
	50% {
		filter: drop-shadow(0 0 50px rgba(255, 255, 255, 0.3));
	}
	100% {
		filter: drop-shadow(0 0 20px rgba(255, 255, 255, 0.4))
	}
}

@keyframes biyikAnim {
	0% {
		transform: rotate(-2deg);
	}
	50% {
		transform: rotate(3deg);
	}
	100% {
		transform: rotate(-2deg);
	}
}
.biyik {
	transform-origin: center center;
	animation: biyikAnim 2s infinite linear;
}

.pages {
	display: flex;
	flex-direction: column;
}

.page {
	min-height: 100vh;
}

.page.intro {
	width: 100vw;
	height: 100vh;
	display: flex;
	align-items: center;
	justify-content: center;
	background: linear-gradient(to bottom, black, #8d0304);
}

.page.history {
	background: linear-gradient(to top, black, #8d0304);
}

.page.outro {
	background: linear-gradient(to bottom, black, #8d0304);
	min-height: unset;
	display: flex;
	align-items: center;
	flex-direction: column;
	justify-content: center;
}

.page.outro .title{
	border-top: 6px solid #fff;
	margin-top: 5rem;
}

.timeline {
	position: relative;
	max-width: 80vw;
	margin: 0 auto;
	display: flex;
	align-items: center;
	justify-content: center;
	flex-direction: column;
}
.timeline .title {
	font-size: 2rem;
	font-weight: bold;
	border-bottom: 6px solid #fff;
	margin-bottom: 2rem;
}
.timeline::after {
	content: '';
	position: absolute;
	width: 6px;
	background-color: white;
	top: 3rem;
	bottom: -5rem;
	margin-left: -3px;
}

.timeline .photos {
	display: flex;
	flex-wrap: wrap;
	justify-content: center;
	align-items: center;
	list-style-type: none;
	margin: 0;
	padding: 0;
}
.timeline .photos li {

}

.timeline .photos img {
	width: 100%;
	border-radius: 0 0 1rem 1rem;
}

.container {
	padding: 1rem;
	position: relative;
	background: #fff;
	border-radius: 1rem;
	width: calc(50% - 5rem);
	color: #333;
}

.container::after {
	content: '';
	position: absolute;
	width: 2rem;
	height: 2rem;
	right: calc(-2rem - 2.2rem);
	background-color: white;
	border: 4px solid #FF9F55;
	top: 0.75rem;
	border-radius: 50%;
	z-index: 1;
}

.container.left {
	align-self: flex-start;
}

.container.right {
	align-self: flex-end;
}

.container.left::before {
	content: '';
	height: 0;
	position: absolute;
	top: 1rem;
	width: 0;
	z-index: 1;
	right: -.6rem;
	border: medium solid white;
	border-width: 1rem 0 1rem 1rem;
	border-color: transparent transparent transparent white;
}

/* Add arrows to the right container (pointing left) */
.container.right::before {
	content: '';
	height: 0;
	position: absolute;
	top: 1rem;
	width: 0;
	z-index: 1;
	left: -.6rem;
	border: medium solid white;
	border-width: 1rem 1rem 1rem 0;
	border-color: transparent white transparent transparent;
}

/* Add arrows to the right container (pointing left) */
.container.right::after {
	left: calc(-2rem - 2.3rem);
}

.container h2, .container h3 {
	margin: 0;
}

.container p {
	margin: 0;
}
</style>
