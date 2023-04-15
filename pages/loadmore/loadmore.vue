<template>
	<view class="load-more">
		<uni-load-more :status="status" :content-text="contentText" @clickLoadMore="clickLoadMore"/>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				status: 'more',
				statusTypes: [{
					value: 'more',
					text: '加载前',
					checked: true
				}, {
					value: 'loading',
					text: '加载中',
					checked: false
				}, {
					value: 'noMore',
					text: '没有更多',
					checked: false
				}],
				contentText: {
					contentdown: '更多小米手机产品',
					contentrefresh: '加载中',
					contentnomore: '没有更多'
				}
			}
		},
		methods: {
			clickLoadMore(e){
				this.status = e.detail.value
			}
		}
	}
</script>

<style lang="scss">
.load-more{
	
}
</style>
