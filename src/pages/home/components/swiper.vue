<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide>
        <img class="swiper-img" src="http://img1.qunarzz.com/sight/p0/1606/c0/c037adf099fd76b490.water.jpg_375x170_cd15a7a1.jpg">
      </swiper-slide>
      <swiper-slide>
        <img class="swiper-img" src="//img1.qunarzz.com/sight/p0/2008/b9/b9cc3ab2fbe4f0e7a3.water.jpg_600x330_41191030.jpg">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      }
    }
  }
}
</script>

<style scoped>
.wrapper{
  width: 100%;
  padding-bottom: 31.25%;
  height: 0;
  overflow: hidden;
  background: #eee;
}
.swiper-img{
  width: 100%;
}
</style>
