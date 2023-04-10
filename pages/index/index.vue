<template>
	<view class="container">
		<nav-bar></nav-bar>
		<swiper-wrap></swiper-wrap>
	</view>
</template>

<script>
	import swiperWrap from '@/pages/swiper/swiper.vue'
	import navBar from '@/pages/nav-bar/nav-bar.vue'
	export default {
		components: {
			swiperWrap,
			navBar
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