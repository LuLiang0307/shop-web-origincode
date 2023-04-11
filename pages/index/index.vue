<template>
	<view class="container">
		<nav-bar></nav-bar>
		<swiper-wrap></swiper-wrap>
		<multi-card></multi-card>
		<rec></rec>
	</view>
</template>

<script>
	import swiperWrap from '@/pages/swiper/swiper.vue'
	import navBar from '@/pages/nav-bar/nav-bar.vue'
	import multiCard from '@/pages/multicard/multicard.vue'
	import rec from '@/pages/rec/rec.vue'
	export default {
		components: {
			swiperWrap,
			navBar,
			multiCard,
			rec
		},
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss" scoped>
	.container {
		font-size: 14px;
		line-height: 24px;
	}
</style>