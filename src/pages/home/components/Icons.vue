<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div v-for="item of page" :key="item.id" class="icon">
            <div class="icon-img">
                <img class="icon-imgcontent" :src="item.imgUel" alt="">
            </div>
            <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      iconList: [{
        id: '001',
        imgUel: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
        desc: '热门景点热门景点热门景点'
      },
      {
        id: '002',
        imgUel: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/69e8b07cb2d438c5530aebd4c8e3abd3.png',
        desc: '一日游'
      },
      {
        id: '003',
        imgUel: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/50357a9f88fe84bcf9d20961059c8611.png',
        desc: '上海迪士尼'
      },
      {
        id: '004',
        imgUel: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/ba632a670497c3393a864595c5411ca1.png',
        desc: '东方明珠'
      },
      {
        id: '005',
        imgUel: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/aba25fb84648c130561afa5398d3552a.png',
        desc: '野生动物园'
      },
      {
        id: '006',
        imgUel: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/aba25fb84648c130561afa5398d3552a.png',
        desc: '上海海昌'
      },
      {
        id: '007',
        imgUel: 'https://imgs.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
        desc: '豫园'
      },
      {
        id: '008',
        imgUel: 'https://imgs.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
        desc: '上海水族馆1'
      },
      {
        id: '009',
        imgUel: 'https://imgs.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
        desc: '豫园'
      },
      {
        id: '010',
        imgUel: 'https://imgs.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
        desc: '上海水族馆1'
      }]
    }
  },
  computed: {
      pages () {
          const pages = []
          this.iconList.forEach((item, index) => {
            const page = Math.floor (index / 8)
            if (!pages[page]) {
                pages[page] = []
            }
            pages[page].push(item)
        })
        return pages
    }
  }
}
</script>

<style scoped>
    .icons >>>.swiper-container{
        height: 0;
        padding-bottom: 50%;
    }
    .icon{
        position: relative;
        overflow: hidden;
        width: 25%;
        height: 0;
        float: left;
        padding-bottom: 25%;
    }
    .icon-img{
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: .44rem;
        box-sizing: border-box;
        padding: .1rem;
    }
    .icon-imgcontent{
        display: block;
        height: 100%;
        margin: 0 auto;
    }
    .icon-desc{
        position: absolute;
        left: 0;
        right: 0;
        bottom: 0;
        line-height: .44rem;
        text-align: center;
        color: #333;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
    }
</style>
