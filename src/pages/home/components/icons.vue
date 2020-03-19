<template>
<div class="icons">
  <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
      <div class="icon"  v-for="item in page" :key="item.id">
      <div class="icon-img"><img :src="item.imgUrl" class="icon-img-content"/></div>
      <p class="icon-word">{{item.name}}</p>
  </div>
  </swiper-slide>
  </swiper>
</div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '001',
        imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/hotel.png',
        name: '酒店'
      }, {
        id: '002',
        imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/flight.png',
        name: '飞机'
      }, {
        id: '003',
        imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/train.png',
        name: '火车票'
      }, {
        id: '004',
        imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/package.png',
        name: '度假'
      }, {
        id: '005',
        imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/piao.png',
        name: '景点门票'
      }, {
        id: '006',
        imgUrl: 'https://picbed.qunarzz.com/f5e5770393d759578962e53ee67798c8.png',
        name: '海外酒店1234'
      }, {
        id: '007',
        imgUrl: 'https://picbed.qunarzz.com/ae617a31e0bd5803d76918b817f6d942.png',
        name: '自由行'
      }, {
        id: '008',
        imgUrl: 'https://picbed.qunarzz.com/1316dc82d1ce6259686d5a68880e5a9d.png',
        name: '攻略'
      }, {
        id: '009',
        imgUrl: 'https://picbed.qunarzz.com/a36d2288f19e54562338f4d8ef986288.png',
        name: '低价机票'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
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

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
   height :0
   padding-bottom : 50%
   .icon
    height :0
    position : relative
    overflow : hidden
    float : left
    width : 25%
    padding-bottom : 25%
    background : #eee
    .icon-img
     display : block
     position :absolute
     top : 6px
     left : 16px
     right :0
     bottom : -10px
     .icon-img-content
      height : 60px
      margin :0 auto
    .icon-word
     padding-top :72px
     text-align :center
     color :$darkTextColor
     ellipsis()
</style>
