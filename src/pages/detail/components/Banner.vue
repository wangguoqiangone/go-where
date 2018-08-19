<template>
	<div>
		<div class="banner" @click="handleBannerClick">
			<img class="banner-img" src="https://dimg04.c-ctrip.com/images/300e0q000000g5o8b658A_C_500_280.jpg" alt="">
			<div class="banner-info">
				<div class="banner-title">国家AAAAA级景区</div>
				<div class="banner-number">
					<span class="iconfont banner-icon">&#xe64b;</span>
					39
				</div>
			</div>
		</div>
		<common-gallary 
			:imgs="imgs" 
			v-show="showGallary"
			@close="handleGallaryClose"
		></common-gallary>
	</div>
</template>

<script>
import CommonGallary from '../../../common/gallary/Gallary'
export default {
	name: 'DetailBanner',
	props: {
		bannerImgs: Array
	},
	data () {
		return {
			showGallary: false,
			imgs: ['https://dimg19.c-ctrip.com/images/10020c000000612i4DDF0_C_500_280.jpg','https://dimg19.c-ctrip.com/images/fd/tg/g4/M0A/32/EE/CggYHlXDE7GAZ7cxADadFdzXxvE947_C_500_280.jpg']
		}
	},
	methods: {
		handleBannerClick () {
			this.showGallary = true
		},
		handleGallaryClose () {
			this.showGallary = false
		}
	},
	components: {
		CommonGallary
	}
}
</script>

<style lang="stylus" scoped>
	.banner
		position: relative
		overflow: hidden
		height: 0
		padding-bottom: 55%
		.banner-img
			width: 100%
		.banner-info
			display: flex
			position: absolute
			left: 0
			right: 0
			bottom: 0
			line-height: .6rem
			color: #fff
			.banner-title
				flex: 1
				font-size: .32rem
				padding: 0 .2rem
			.banner-number
				height: .32rem
				line-height: .32rem
				margin-top: .14rem
				padding: 0 .4rem
				border-radius: .2rem
				background: rgna(0, 0, 0, .8)
				font-size: .24rem
				.banner-icon
					font-size: .24rem
</style>