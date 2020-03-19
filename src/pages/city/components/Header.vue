<template>
  <div>
    <div class="header">城市选择
    <router-link to="/"><div class="iconfont header-back">&#xe610;</div></router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "CityHeader"
};
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header
 position : relative
 overflow: hidden
 height: $headerHeight
 line-height: $headerHeight
 text-align: center
 color: #fff
 background: $bgColor
 .header-back
  width :12px
  text-align :center
  font-size :18px
  position :absolute
  top:0
  left:3px
  color :white
</style>
