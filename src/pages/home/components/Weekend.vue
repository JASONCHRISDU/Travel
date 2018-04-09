<template>
	<div>
		<div class="title">週末旅遊好去處</div>
		<ul>
			<li class="item border-bottom" v-for="item in recommendList" :key="item.id">
				<div class="item-img-wrapper">
					<img class="item-img" :src="item.imgUrl" alt="" />
				</div>
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
				</div>
			</li>
		</ul>
	</div>
</template>
<script>
	export default {
		name: 'HomeWeekend',
		data() {
			return {
				recommendList: [
					{
						id: '001',
						imgUrl: '//img1.qunarzz.com/sight/source/1505/9f/f585152825459.jpg_r_640x214_5d46e4cc.jpg',
						title: '南山文化旅游区',
						desc: '看108米高的“南山海上观音”，其造型挺拔，气势恢宏！'
					},
					{
						id: '002',
						imgUrl: '//img1.qunarzz.com/sight/source/1505/9f/f585152825459.jpg_r_640x214_5d46e4cc.jpg',
						title: '南山文化旅游区',
						desc: '看108米高的“南山海上观音”，其造型挺拔，气势恢宏！'
					},
					{
						id: '003',
						imgUrl: '//img1.qunarzz.com/sight/source/1505/9f/f585152825459.jpg_r_640x214_5d46e4cc.jpg',
						title: '南山文化旅游区',
						desc: '看108米高的“南山海上观音”，其造型挺拔，气势恢宏！'
					},
					{
						id: '004',
						imgUrl: '//img1.qunarzz.com/sight/source/1505/9f/f585152825459.jpg_r_640x214_5d46e4cc.jpg',
						title: '南山文化旅游区',
						desc: '看108米高的“南山海上观音”，其造型挺拔，气势恢宏！'
					},					
				]
			}
		}
	}
</script>
<style lang="stylus" scoped>
	@import '~styles/mixins.styl'
	.title
		margin-top: .2rem
		line-height: .8rem
		text-indent: .2rem
		background: #eee
	.item-img-wrapper	
		overflow: hidden
		padding-bottom: 30%
		height: 0			
		.item-img
			width: 100%
	.item-info
		padding: .1rem
		.item-title
			ellipsis()				
			line-height: .54rem
			font-size: .32rem
		.item-desc
			ellipsis()
			line-height: .4rem
			color: #ccc
</style>