<template>
	<view class="nav-bar">
		<uni-nav-bar :fixed="true" background-color="#F5F5F6" status-bar right-icon="person" leftWidth="0px" rightWidth="30px"
			title="自定义导航栏">
			<view class="input-view">
				<uni-easyinput prefixIcon="search" v-model="value" placeholder="搜索商品名称" @iconClick="iconClick"
					:trim="true"></uni-easyinput>
			</view>			
		</uni-nav-bar>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				value: ''
			}
		},
		methods: {
			iconClick() {}
		}
	}
</script>

<style lang='scss'>
	.nav-bar{
		.input-view {
			/* #ifndef APP-PLUS-NVUE */
			display: flex;
			/* #endif */
			flex-direction: row;
			align-items: center;
			flex: 1;
			flex-wrap: nowrap;
			width: 120px;
		}		
	}
</style>
