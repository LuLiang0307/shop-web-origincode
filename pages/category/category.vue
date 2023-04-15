<template>
	<view class="category">		
		<uni-card>
			<uni-nav-bar :fixed="true" background-color="#F5F5F6" status-bar leftWidth="0px" rightWidth="0px" title="自定义导航栏">
				<view class="input-view">
					<uni-easyinput prefixIcon="search" v-model="value" placeholder="搜索商品名称" @iconClick="iconClick"
						:trim="true"></uni-easyinput>
				</view>
			</uni-nav-bar>
			<menu-side-bar></menu-side-bar>
			</uni-card>
	</view>
</template>

<script>
	import menuSideBar from '../menusidebar/menusidebar.vue'
	export default {
		components:{
			menuSideBar
		},
		data() {
			return {
				value: '',
			}
		},
		methods: {
			iconClick() {}
		}
	}
</script>

<style lang="scss">
	.category {
		background-color: #F5F5F6;
			.input-view {
				/* #ifndef APP-PLUS-NVUE */
				display: flex;
				/* #endif */
				flex-direction: row;
				align-items: center;
				flex: 1;
				flex-wrap: nowrap;
				width: 100%;
			
		}
	}
</style>