<template>
<div class="header">
  <div class="header-left"><div class="iconfont back-btn">&#xe610;</div></div>
  <div class="header-input"><span class="iconfont">&#xe69d;</span>输入城市/景点/游玩主题</div>
  <div class="header-right">城市<span class="iconfont">&#xe612;</span></div>
</div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
//    1rem = html font-size = 50px
    @import '~styles/varibles.styl'
    .header
        height:55px
        display :flex
        background : $bgColor
        line-height :55px
        color :#fff
        .header-left
            width:54px
            float : left
            .back-btn
              text-align :center
              font-size :24px
        .header-input
            padding-left :5px
            flex : 1
            background :#fff
            border-radius :8px
            margin-top : 5px
            height :45px
            color:#ccc
            line-height :45px
        .header-right
            width : 84px
            float : right
            text-align :center
</style>
