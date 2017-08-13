<style src="./image-slider.css"/>

<template>
<div class="component-image-slider" tabindex="0">
<div :style="{ left: leftPosition }" class="slides">
	<picture v-for="url in images" class="slide" :key="url"><img :src="url" alt=""></picture>
 </div>
	<button v-if="canGoPrev" @click="prev" class="prev">&#10094;</button>
	<button v-if="canGoNext" @click="next" class="next">&#10095;</button>
</div>
</template>

<script>
export default {
	components: {},
	props: {
		images: Array
	},
	data() {
		return {
			index: 0
		};
	},
	computed: {
		length() {
			return this.images.length;
		},
		canGoNext() {
			return this.index < this.length - 1;
		},
		canGoPrev() {
			return this.index > 0;
		},
		leftPosition() {
			const unit = '%';
			const left = -100 * this.index;
			return left + unit;
		}
	},
	methods: {
		prev() {
			if (!this.canGoPrev) {
				return;
			}
			this.index -= 1;
		},
		next() {
			if (!this.canGoNext) {
				return;
			}
			this.index += 1;
		}
	},

};
</script>

<!--
http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/ChevroletCorvetteZO6_MayDLC_ForzaHorizon2_01_WM.jpg

http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/14442c5e-1063-48d9-9850-537615e0333a.jpg.jpg

http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/1409758275_2012-jaguar-xkr-s.jpg


-->