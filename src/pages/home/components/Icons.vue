<template>
	<div class="icons">
		<swiper>	    
		    <swiper-slide v-for="(page, index) of pages" :key="index"> 
				<div class="icon" v-for="item in page" :key="item.id">
					<div class="icon-img">
						<img class="icon-img-content" :src="item.imgUrl" />
					</div>	
					<p class="icon-desc">{{item.desc}}</p>
				</div>
		    </swiper-slide>				    
		</swiper>
	</div>
</template>

<script>
	export default {
		name: 'HomeIcons',
		data() {
			return {
				iconsList: [
					{
						id: '001',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
						desc: '熱門景點'
					},
					{
						id: '002',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
						desc: '櫻花季'
					},
					{
						id: '003',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
						desc: '賞雪季'
					},
					{
						id: '004',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
						desc: '泡溫泉'
					},
					{
						id: '005',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
						desc: '一日遊'
					},
					{
						id: '006',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
						desc: '極光震撼'
					},
					{
						id: '007',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
						desc: '峽谷灣區'
					},
					{
						id: '008',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
						desc: '富士山'
					},
					{
						id: '009',
						imgUrl: '//img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
						desc: '開學季'
					}
				]
			}
		},
		computed: {
			pages() {
				const pages = [];
				this.iconsList.forEach((item, index) => {
					const page = Math.floor(index / 8)
					if(!pages[page]) {
						pages[page] = []
					}
					pages[page].push(item)
				})
				return pages;
			}
		}
	}
</script>

<style lang="stylus" scoped>
	@import '~styles/varibles.styl'
	@import '~styles/mixins.styl'
	.icons	
		overflow: hidden		
		padding-bottom: 50%
		height: 0
		.icon
			overflow: hidden
			float: left
			position: relative
			padding-bottom: 25%
			width: 25%
			height: 0
			.icon-img
				box-sizing: border-box
				position: absolute		
				top: 0
				left: 0
				right: 0
				bottom: .44rem
				padding: .1rem
				.icon-img-content
					display: block
					margin: 0 auto
					height: 100%
			.icon-desc
				ellipsis()				
				position: absolute
				left: 0
				right: 0
				bottom: 0
				height: .44rem
				text-align: center
				line-height: .44rem				
				color: $darkTextColor
</style>