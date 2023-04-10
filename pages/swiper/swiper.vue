<template>
	<view class="uni-margin-wrap">
		<swiper class="swiper" circular @change="change" :indicator-dots="indicatorDots" :autoplay="autoplay"
			:interval="interval" :duration="duration">
			<swiper-item v-for="(item ,index) in info" :key="index">
				<view class="swiper-item">
					<image :src="item.src" alt=""></image>
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: [{
						src: '/static/swiper-img/swiper1.png'
					},
					{
						src: '/static/swiper-img/swiper2.png'
					},
					{
						src: '/static/swiper-img/swiper3.png'
					},
				],
				indicatorDots: true,
				autoplay: true,
				duration: 500,
				interval: 3000,
			}
		},
		methods: {
			change(e) {
				this.current = e.detail.current;
			}		
			
		}
	}
</script>

<style lang="scss">
.uni-margin-wrap {
	width: 100%;
	.swiper {
		height: calc(100vw*540/1080);

		uni-image {
			width: 100%;
			height: calc(100vw*540/1080);
		}
	}

}
</style>
