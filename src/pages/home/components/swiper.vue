<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img :src="item.imgUel" alt="" class="swiper-img">
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
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '001',
        imgUel: 'http://img1.qunarzz.com/sight/p0/1606/c0/c037adf099fd76b490.water.jpg_375x170_cd15a7a1.jpg'
      },
      {
        id: '002',
        imgUel: '//img1.qunarzz.com/sight/p0/2008/b9/b9cc3ab2fbe4f0e7a3.water.jpg_600x330_41191030.jpg'
      }]
    }
  }
}
</script>

<style scoped>
.wrapper{
  width: 100%;
  padding-bottom: 55%;
  height: 0;
  overflow: hidden;
  background: #eee;
}
.swiper-img{
  width: 100%;
}
.wrapper >>> .swiper-pagination-bullet-active{
  background: #fff;
}
</style>
