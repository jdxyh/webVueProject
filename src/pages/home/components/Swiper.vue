<template>
  <!--解决画面抖动-->
  <div class = "wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <!--做循环输出-->
      <swiper-slide v-for="item of list" :key = "item.id">
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
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
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
    padding-bottom: 28%
    background: #eee
    .swiper-img
      width: 100%
</style>
