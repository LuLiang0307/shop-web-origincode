<template>
	<view class="nothing">
		<text>更多功能正在开发中……</text>
		<img src="/static/kaifazhong.jpeg" alt="">
		
	</view>
</template>

<script>
	export default {
		onLoad: function(option){
			console.log(option.title)
		},
		data() {
			return {
			}
		},
		methods: {
		}
	}
</script>

<style lang="scss">
.nothing{
	display: flex;
	flex-direction: column;
	vertical-align: middle;
	align-items: center;
	text{
		color: rgb(60, 197, 31);
	}
	img{
		flex: 1;
		width: 60%;
	}
}
</style>
