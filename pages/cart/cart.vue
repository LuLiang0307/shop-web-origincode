<template>
	<view class="cart">
		<uni-nav-bar shadow left-icon="left" leftText="返回" rightText="编辑" title="购物车" height="50px"/>
		<uni-card :title="shopName">
			
		</uni-card>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				shopName: '小米自营'
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.cart{
		.uni-card{
			margin: 10px !important;
			border-radius: 10px;
			
		}
	}
</style>
