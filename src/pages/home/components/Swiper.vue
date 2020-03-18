<template>
<div class="wrapper">
    <swiper :options="swiperOption">
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
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '001',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20201/86ca4dc2777b997607e97eb8471dcafd.jpg_890x330_0eee7728.jpg'
      }, {
        id: '002',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20201/8216fd250c35366befc35f6353f934b9.jpg_890x330_9062b3ba.jpg'
      }, {
        id: '003',
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/30/cea146e3d2eda002.jpg_890x330_f72cb574.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background : white !important
  .wrapper
    width :100%
    height :0
    overflow :hidden
    padding-bottom :37.07%
    background #eee
    .swiper-img
        width :100%
</style>
