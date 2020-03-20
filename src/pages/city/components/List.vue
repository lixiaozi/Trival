<template>
  <div class="list" ref="wrapper">
      <div>
      <div class="area">
          <div class="title boder-topbottom">当前城市</div>
          <div class="button-list">
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
               <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
          </div>
      </div>
      <div class="area">
          <div class="title boder-topbottom">热门城市</div>
          <div class="button-list">
              <div class="button-wrapper" v-for="item of hot" :key="item.id">
                  <div class="button">{{item.name}}</div>
              </div>
          </div>
      </div>
      <div class="area" v-for="(item, key) of cities" :key="key">
          <div class="title boder-topbottom">{{key}}</div>
          <div class="item-list">
              <div class="item" v-for="innerItem of item" :key="innerItem.id">{{innerItem.name}}</div>
          </div>
        </div>
     </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    hot:Array,
    cities:Object
  },
  mounted () {
      this.scroll = new Bscroll(this.$refs.wrapper)
  },
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.list
 overflow: hidden
 position: absolute
 top ::102px
 left :0
 right:0
 bottom :0
 .boder-topbottom
  border :1px solid #ccc
//   &:before
//     border-color :#ccc
//   &:after
//     border-color :#ccc
 .title
  line-height : 28px
  background :#eee
  padding-left : 20px
  color :#666
 .button-list
  overflow : hidden
  padding :10px 30px 10px 10px
  .button-wrapper
   float : left 
   width : 33.33%
   .button 
    padding :2px
    border :1px solid #ccc
    text-align :center
    width :75px
    border-radius :5px
.item-list
 .item
  padding-left :20px
  border-bottom : 1px solid #ccc
  line-height :28px

</style>
