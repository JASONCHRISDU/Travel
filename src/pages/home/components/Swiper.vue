<template>
	<div class="wrapper">
		<swiper :options="swiperOption" v-if="showSwiper">	    
		    <swiper-slide v-for="item in list" :key="item.id">
		    	<img class="swiper-img" :src="item.imgUrl" alt="" />
		    </swiper-slide>		    
		    <div class="swiper-pagination" slot="pagination"></div>	    	    
		</swiper>
	</div>
</template>
<script>
	export default {
		name: 'HomeSwiper',
		props: {
			list: Array
		},
		data() {
			return {
				swiperOption: {
					pagination: '.swiper-pagination',
					loop: true
				},
				swiperList: [
					{
						id: '001',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1802/51/e78f936a5b404102.jpg_640x200_c14f0b3a.jpg'
					},
					{
						id: '002',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1803/98/0a2e0bd8eb0c0802.png_640x200_0aae3331.png'
					}
				]
			}
		},
		computed: {
			showSwiper() {
				return this.list.length
			}
		}

	}
</script>
<style lang="stylus" scoped>
	.wrapper >>> .swiper-pagination-bullet-active
		background: #fff
	.wrapper
		overflow: hidden
		padding-bottom: 31.25%
		width: 100%
		height: 0
		background: #eee		
		.swiper-img
			width: 100%
	
</style>