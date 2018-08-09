<template>
	<div>
		<div class="title">热销推荐</div>
		<ul>
			<li calss="item" v-for="item of List" :key="item.id">
				<img class="item-img" :src="item.imgUrl" />
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					<button class="item-button">查看详情</button>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
export default {
	name: 'HomeRecommend',
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
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
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
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff	
</style>