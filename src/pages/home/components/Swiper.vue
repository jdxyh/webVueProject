<template>
  <!--解决画面抖动-->
  <div class = "wrapper">
    <swiper :options="swiperOption">
      <!--做循环输出-->
      <swiper-slide v-for="item of swiperList" :key = "item.id">
        <img class = "swiper-img" :src = "item.imgUrl"/>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '01',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg'
      }, {
        id: '02',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1708/7c/c0b9acba07764302.jpg_750x200_389436b7.jpg'
      }, {
        id: '03',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/e8/14b75b1c81fbe702.jpg_750x200_e6d4f1f1.jpg'
      }]
    }
  }
}
</script>

<style lang = "stylus" scoped>
  //组件样式进行穿透
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 27%
    background: #eee
    .swiper-img
      width: 100%
</style>
