<template>
  <!--解决画面抖动-->
  <div clsass = "wrapper">
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide>
      <img class = "sper-img" src = "@/assets/imgs/swiper/1.jpg"/>
    </swiper-slide>
    <swiper-slide>
      <img src = "@/assets/imgs/swiper/2.jpg"/>
    </swiper-slide>
    <swiper-slide>
      <img src = "@/assets/imgs/swiper/3.jpg"/>
    </swiper-slide>
    <swiper-slide>
      <img src = "@/assets/imgs/swiper/4.jpg"/>
    </swiper-slide>
    <swiper-slide>
      <img src = "@/assets/imgs/swiper/5.jpg"/>
    </swiper-slide>
    <swiper-slide>
      <img src = "@/assets/imgs/swiper/6.jpg"/>
    </swiper-slide>
    <swiper-slide>
      <img src = "@/assets/imgs/swiper/7.jpg"/>
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
      swiperOption: {}
    }
  }
}
</script>

<style lang = "stylus" scoped>
  .swiper-img{
    width:100%
  }
  //解决画面抖动方案
  .wrapper{
    overflow hidden
    width:100%
    height 0
    padding-bottom 31.25%
  }
</style>
