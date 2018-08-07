<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for="item of swiperList" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      /*轮播图的圆点*/
      swiperOption: {
        pagination: '.swiper-pagination',
        /*是否循环*/
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://dimg19.c-ctrip.com/images/10020e00000070mc3FB1C_C_500_280_Q90.jpg'
      },{
        id: '0002',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100n0b0000005w11rA282.jpg'
      },{
        id: '0003',
        imgUrl: 'https://dimg18.c-ctrip.com/images/100l0b0000005xwkp070E_C_500_280.jpg'
      },{
        id: '0004',
        imgUrl: 'https://dimg06.c-ctrip.com/images/350l0n000000ec6k84D0F_C_640_360.jpg'
      },{
        id: '0005',
        imgUrl: 'http://images4.c-ctrip.com/target//fd/tg/g2/M07/12/50/CghzgVU0ZvGAA-J0AAFAvvtb4iw891.jpg'
      }]
    }
  }
}
</script>
<!-- 设置全局的轮播图点的样式 -->
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    .swiper-img
      width: 100%
</style>