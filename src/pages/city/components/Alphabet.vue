<template>
  <ul class="list">
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
 .list
  position :absolute
  top:140px
  right :4px
  bottom:100px
  display :flex
  flex-direction : column
  justify-content : center
  width :15px
  .item
   line-height :18px
   text-align : center
   color : $bgColor
</style>
