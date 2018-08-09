<template>
	<div>
		<div class="title">周末去哪儿</div>
		<ul>
			<li calss="item" v-for="item of List" :key="item.id">
				<div class="item-img-wrapper">
					<img class="item-img" :src="item.imgUrl" />
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
	data () {
		return {
			List: [{
				id: '0001',
				imgUrl: 'https://dimg19.c-ctrip.com/images/10020e00000070mc3FB1C_C_500_280_Q90.jpg',
				title: '这是一个标题',
				desc: '这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题'
			},{
				id: '0002',
				imgUrl: 'https://dimg19.c-ctrip.com/images/10020e00000070mc3FB1C_C_500_280_Q90.jpg',
				title: '这是一个标题',
				desc: '这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题'
			},{
				id: '0003',
				imgUrl: 'https://dimg19.c-ctrip.com/images/10020e00000070mc3FB1C_C_500_280_Q90.jpg',
				title: '这是一个标题',
				desc: '这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题'
			},{
				id: '0004',
				imgUrl: 'https://dimg19.c-ctrip.com/images/10020e00000070mc3FB1C_C_500_280_Q90.jpg',
				title: '这是一个标题',
				desc: '这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题这是一个标题'
			}]
		}
	}
}
</script>
	
<style lang="stylus" scoped>
@import '~@/assets/styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
  	overflow: hidden
  	height: 0
  	padding-bottom: 33.9%
		.item-img
	  	width: 100%
	.item-info
	  flex: 1
	  padding: .1rem
	  min-width: 0
	  .item-title
	    line-height: .54rem
	    font-size: .32rem
	    ellipsis()
	  .item-desc
	    line-height: .4rem
	    color: #ccc
	    ellipsis()
</style>