<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或拼音"/>
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
    .search
     height : 40px
     padding 0 12px 5px 12px
     background : $bgColor
     .search-input
      box-sizing : border-box
      padding 2px 5px
      width :100%
      height :32px
      line-height :32px
      text-align :center
      border-radius :5px
      color :#666
</style>
