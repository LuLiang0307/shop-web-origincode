<template>
	<view class="multi-card">
		<uni-card>
			<view class="row1">
				<view class="card" v-for="(item, index) in info[0]" :key="index">
					<img :src="item.src" alt="">
				</view>
			</view>
			<view class="row2">
				<view class="card" v-for="(item, index) in info[1]" :key="index">
					<img :src="item.src" alt="">
				</view>
			</view>
			
		</uni-card>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info:{0:[
						{src: '/static/multi-icon/1.png', text: '米金商城'},
						{src: '/static/multi-icon/2.png', text: '小米众筹'},
						{src: '/static/multi-icon/3.png', text: '手机'},
						{src: '/static/multi-icon/4.png', text: '以旧换新'},
						{src: '/static/multi-icon/5.png', text: '小米上新'}
					],
					1:[
						{src: '/static/multi-icon/6.png', text: '智能'},
						{src: '/static/multi-icon/7.png', text: '笔记本热卖'},
						{src: '/static/multi-icon/8.png', text: '电视热卖'},
						{src: '/static/multi-icon/9.png', text: '洗衣机热卖'},
						{src: '/static/multi-icon/10.png', text: '米粉卡'}
					]
				}
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.multi-card{
		padding: 0 !important;margin: 0 !important;
		.uni-card{
			.uni-card__content{
				display: flex;
				flex-direction: row;
				flex-wrap: wrap;
				.row1,.row2{
					display: flex;
				}
				.card{
					img{
						width: 100%;
						
					}
				}
			}
		}
		 
	}
</style>
