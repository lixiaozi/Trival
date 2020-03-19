<template>
<div>
    <div class="recommend-title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wraper"><img class="item-img" :src="item.imgUrl"/></div>
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
          </div>
      </li>
    </ul>
</div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'https://imgs.qunarzz.com/p/tts4/1810/f6/324ab8cce55bc602.jpg_r_480x320x90_e05f8f5f.jpg',
        title: 'dalian1234',
        desc: '2222222222222'
      }, {
        id: '002',
        imgUrl: 'https://imgs.qunarzz.com/p/tts4/1810/f6/324ab8cce55bc602.jpg_r_480x320x90_e05f8f5f.jpg',
        title: 'dalian1234',
        desc: '2222222222222'
      }, {
        id: '003',
        imgUrl: 'https://imgs.qunarzz.com/p/tts4/1810/f6/324ab8cce55bc602.jpg_r_480x320x90_e05f8f5f.jpg',
        title: 'dalian1234',
        desc: '2222222222222'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .recommend-title
    margin-top : 2px
    line-height : 30px
    background : #eeeeee
    text-indent : 20px
  .item-img-wraper
    overflow : hidden
    height : 0
    padding-bottom : 39.7%
    .item-img
     width : 100%
    .item-info
     padding : 2px
     .item-title
      line-height : 30px
      font-size : 18px
     .item-desc
      line-height :25px
      color : #666666
      font-size : 14px
      margin-top : -7px
</style>
