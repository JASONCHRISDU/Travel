<template>
	<div>
		<div class="title">熱賣推薦</div>
		<ul>
			<li class="item border-bottom" v-for="item in list" :key="item.id">
				<img class="item-img" :src="item.imgUrl" alt="" />
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					<button class="item-button">查看詳情</button>
				</div>
			</li>
		</ul>
	</div>
</template>
<script>
	export default {
		name: 'HomeRecommend',
		props: {
			list: Array
		},
		data() {
			return {
				recommendList: [
					{
						id: '001',
						imgUrl: '//img1.qunarzz.com/wugc/p189/201206/12/a3ace34bc010041193835fbb.jpg_200x200_84bd8f96.jpg',
						title: '南山文化旅游区',
						desc: '看108米高的“南山海上观音”，其造型挺拔，气势恢宏！'
					},
					{
						id: '002',
						imgUrl: '//img1.qunarzz.com/wugc/p189/201206/12/a3ace34bc010041193835fbb.jpg_200x200_84bd8f96.jpg',
						title: '南山文化旅游区',
						desc: '看108米高的“南山海上观音”，其造型挺拔，气势恢宏！'
					},
					{
						id: '003',
						imgUrl: '//img1.qunarzz.com/wugc/p189/201206/12/a3ace34bc010041193835fbb.jpg_200x200_84bd8f96.jpg',
						title: '南山文化旅游区',
						desc: '看108米高的“南山海上观音”，其造型挺拔，气势恢宏！'
					},
					{
						id: '004',
						imgUrl: '//img1.qunarzz.com/wugc/p189/201206/12/a3ace34bc010041193835fbb.jpg_200x200_84bd8f96.jpg',
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
	.item
		overflow: hidden
		display: flex
		height: 1.9rem			
		.item-img
			padding: .1rem
			width: 1.7rem
			height: 1.7rem
		.item-info
			flex: 1
			padding: .1rem
			min-width: 0
			.item-title
				ellipsis()				
				line-height: .54rem
				font-size: .32rem
			.item-desc
				ellipsis()
				line-height: .4rem
				color: #ccc
			.item-button
				margin-top: .2rem
				padding: 0 .2rem
				font-size: .2rem
				letter-spacing: .04rem
				background: #ff9300
				border-radius: .06rem
				color: #fff
</style>