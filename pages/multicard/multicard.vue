<template>
	<view class="multi-card">
		<uni-card>
			<view class="row1">
				<view class="card" v-for="(item, index) in info[0]" :key="index" @click="intoInfo(item)">
					<img :src="item.src" alt="">
				</view>
			</view>
			<view class="row2">
				<view class="card" v-for="(item, index) in info[1]" :key="index" @click="intoInfo(item)">
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
						{id: '1',src: '/static/multi-icon/1.png', text: '米金商城'},
						{id: '2',src: '/static/multi-icon/2.png', text: '小米众筹'},
						{id: '3',src: '/static/multi-icon/3.png', text: '手机'},
						{id: '4',src: '/static/multi-icon/4.png', text: '以旧换新'},
						{id: '5',src: '/static/multi-icon/5.png', text: '小米上新'}
					],
					1:[
						{id: '6',src: '/static/multi-icon/6.png', text: '智能'},
						{id: '7',src: '/static/multi-icon/7.png', text: '笔记本热卖'},
						{id: '8',src: '/static/multi-icon/8.png', text: '电视热卖'},
						{id: '9',src: '/static/multi-icon/9.png', text: '洗衣机热卖'},
						{id: '10',src: '/static/multi-icon/10.png', text: '米粉卡'}
					]
				}
			}
		},
		methods: {
			intoInfo(e){
				uni.navigateTo({
					url: '/pages/nothing/nothing'
				})
			}
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
