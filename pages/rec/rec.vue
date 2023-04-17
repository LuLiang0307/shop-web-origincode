<template>
	<view class="grid-container rec">
		<img :class="item.class" v-for="(item, index) in info" :key="index" :src="item.src" alt="item.text" @click="intoInfo(item)">
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: [{
						src: '/static/rec-img/1.png',
						text: '1',
						class: 'box1'
					},
					{
						src: '/static/rec-img/2.png',
						text: '2',
						class: 'box2'
					},
					{
						src: '/static/rec-img/3.png',
						text: '3',
						class: 'box3'
					},
				]
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
	.rec {
		margin: 10px 0;

		&.grid-container {
			display: grid;

			.box1 {
				grid-area: box1;
			}

			.box2 {
				grid-area: box2;
			}

			.box3 {
				grid-area: box3;
			}

			grid-template-columns: 1fr 1fr;
			grid-template-rows: 1fr 1fr;
			grid-template-areas: "box1  box2"
			"box1  box3";
			grid-column-gap: 3px;
			grid-row-gap: 2px;
			img {
				width: 100%;
			}
		}
	}
</style>