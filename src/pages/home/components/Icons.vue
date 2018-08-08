<template>
	
	<div class="icons"><!-- 用来做宽高比例2:1 -->
		<swiper>
			<swiper-slide v-for="(page, index) of pages" :key="index">
				<div 
					class="icon" 
					v-for="item of page"
					:key="item.id"
				>
						<div class="icon-img">
							<img class="icon-img-content" :src="item.imgUrl"/>
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
	data () {
		return {
			iconList: [{
					id: '0001',
					imgUrl: 'https://pages.ctrip.com/hotel_h5/res/img/index-inn.png?20180731191122j',
					desc: '景点门票'
				},{
					id: '0002',
					imgUrl: 'https://pages.ctrip.com/hotel_h5/res/img/index-hourroom.png?20180731191122j',
					desc: '哈撒ki'


				},{
					id: '0003',
					imgUrl: 'https://pages.ctrip.com/hotel_h5/res/img/index-hourroom.png?20180731191122j',
					desc: '哈撒ki'
				},{
					id: '0004',
					imgUrl: 'https://pages.ctrip.com/hotel_h5/res/img/index-find.png?20180731191122j',
					desc: '哈撒ki'
				},{
					id: '0005',
					imgUrl: 'https://pages.ctrip.com/hotel_h5/res/img/index-hourroom.png?20180731191122j',
					desc: '哈撒ki'


				},{
					id: '0006',
					imgUrl: 'https://pages.ctrip.com/hotel_h5/res/img/index-hourroom.png?20180731191122j',
					desc: '哈撒ki'
				},{
					id: '0007',
					imgUrl: 'https://pages.ctrip.com/hotel_h5/res/img/index-find.png?20180731191122j',
					desc: '哈撒ki'
				},{
					id: '0008',
					imgUrl: 'https://pages.ctrip.com/hotel_h5/res/img/index-hourroom.png?20180731191122j',
					desc: '哈撒ki'


				},{
					id: '0009',
					imgUrl: 'https://pages.ctrip.com/hotel_h5/res/img/index-hourroom.png?20180731191122j',
					desc: '哈撒ki'
				},{
					id: '0010',
					imgUrl: 'https://pages.ctrip.com/hotel_h5/res/img/index-find.png?20180731191122j',
					desc: '哈撒ki'
				}]
		}
	},
	computed: {
		pages () {
			const pages = []
			this.iconList.forEach((item, index) => {
				const page = Math.floor(index / 8)
				if(!pages[page]) {
					pages[page] = []
				}
				pages[page].push(item)
			})
			return pages
		}
	}
}
</script>

<style lang="stylus" scoped>
	@import '~@/assets/styles/varibles.styl'
	@import '~@/assets/styles/mixins.styl'
	.icons >>> .swiper-container
		height: 0
		padding-bottom: 50%
	.icons
		overflow: hidden
		height: 0
		padding-bottom: 50%
		.icon
			position: relative
			float: left
			width: 25%
			height: 0
			padding-bottom: 25%
			.icon-img
				postion: absolute
				top: 0
				left: 0
				right: 0
				bottom: .44rem
				.icon-img-content
					height: 0
					display: block
					margin: 0 auto
					height: 100%
			.icon-desc
				position: absolute
				left: 0
				right: 0
				bottom: 0
				height: .44rem
				line-height: .44rem
				text-align: center
				color: $darkTextColor
				ellipsis()

</style>