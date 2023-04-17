<template>
	<view class="hot-goods">
		<uni-card>
			<img class="big-img" src="/static/hot.png" alt="" @click="intoInfo">
			<uni-grid :column="2" borderColor="#fff">
				<uni-grid-item v-for="(item, index) in info" :key="index">
					<view class="grid-item-box">
						<img :src="item.src" alt="">
						<uni-title type="h4" :title="item.title" align="center"></uni-title>
						<text class="text">{{item.text}}</text>
						<text class="price" type="h5" align="center">￥{{item.price}}起</text>
						<button type="warn" size="mini" @click="intoInfo">立即购买</button>							
					</view>
				</uni-grid-item>
			</uni-grid>
			<load-more></load-more>
		</uni-card>

	</view>
</template>

<script>
	import loadMore from '@/pages/loadmore/loadmore.vue'
	export default {
		components:{
			loadMore
		},
		data() {
			return {
				info:[
					{src: '/static/goods/1.png', text:'2k直屏的狠旗舰',title: 'Redmi K50', price: '2099'},
					{src: '/static/goods/2.png', text:'小尺寸性能旗舰|徕卡影像',title: 'Xiaomi 12S', price: '3399'},
					{src: '/static/goods/3.png', text:'全新骁龙8|2K AMOLED屏幕',title: 'Xiaomi 12 Pro', price: '4199'},
					{src: '/static/goods/4.png', text:'三星AMOLED高刷屏',title: 'Note 11 Pro系列', price: '1799'},
				],
				
			}
		},
		methods: {
			clickAt(){
				
			},
			intoInfo(){
				uni.navigateTo({
					url: '/pages/nothing/nothing'
				})
			}
		}
	}
</script>

<style lang="scss">
	.hot-goods{
		.uni-card{
			.uni-card__content{
				display: flex;
				flex-direction: column !important;
				.big-img{
					margin-top: -1px;
					width: 100%;
				}
				.uni-grid-item{
					height: auto !important;
					margin: 10px 0;
					.grid-item-box{
						display: flex;
						flex-direction: column;
						align-items: center;
						vertical-align: middle;
						img{
							width: 98%;
							margin: 0 3px;
						}
						.uni-title__box{
							margin: 0;padding: 0 ;
						}
						.text{
							text-align: center;
							font-size: 12px;
						}
						.price{
							color: #e64340;
							font-weight: 500;
						}					
					}	
				}
			}
		}
	}
</style>
