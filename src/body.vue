<script>
import ImageSlider from './components/image-slider/image-slider.vue';

export default {
	components: {
		ImageSlider,
	},
	data() {
		return {
			images: [
				'https://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/ChevroletCorvetteZO6_MayDLC_ForzaHorizon2_01_WM.jpg',

				'https://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/14442c5e-1063-48d9-9850-537615e0333a.jpg.jpg',

				'http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/1409758275_2012-jaguar-xkr-s.jpg',

				'https://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/1411800820_nissangt-r_wm_carreveal_week6_forzahorizon21.jpg'
			],
		};
	}
};
</script>

<style>
body, html {
	width: 100%;
	height: 100%;
	padding: 0;
	margin: 0;
}

body {
	box-sizing: border-box;
	padding: 20px;
}


	</style>
<template>
  <body>

	<image-slider class="image-slider" :images="images"/>
  </body>
</template>