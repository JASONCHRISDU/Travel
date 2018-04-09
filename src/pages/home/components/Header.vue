<template>
	<div class="header">	
		<div class="header-left">
			<div class="iconfont back-icon">&#xe624;</div>
		</div>
		<div class="header-input">
			<span class="iconfont">&#xe632;</span>
			輸入相關搜尋關鍵字
		</div>
		<div class="header-right">
			城市
			<span class="iconfont arrow-icon">&#xe62d;</span>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'HomeHeader'
	}
</script>

<style lang="stylus" scoped>
	@import '~styles/varibles.styl'
	.header
		display: flex
		line-height: .86rem		
		color: #fff
		background: $bgColor
		.header-left
			float: left
			width: .64rem
			.back-icon				
				font-size: .4rem
				text-align: center
		.header-input
			flex: 1
			margin-top: .12rem
			margin-left: .2rem
			padding-left: .2rem
			height: .64rem		
			line-height: .64rem	
			color: #ccc
			background: #fff
			border-radius: .1rem
		.header-right
			float: right
			width: 1.24rem			
			text-align: center
			.arrow-icon
				font-size: .2rem
</style>