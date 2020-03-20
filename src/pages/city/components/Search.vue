<template>
  <div>
    <div class="search">
    <input v-model="keyword" class="search-input" type="text" placeholder="输入城市名或拼音"/>
    </div>
    <div class="search-content" ref="search" v-show="keyword">
      <ul>
        <li class="search-item " v-for="item of list" :key="item.id">{{item.name}}</li>
        <li class="search-item " v-show="hasList">no find</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  computed: {
    hasList(){
      return !this.list.length
    }
  },
   watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if(!this.keyword) {
        this.list = []
        return
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 || value.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  }
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
<<<<<<< HEAD
</style>
=======
  .search-content
    overflow : hidden
    position : absolute
    top:100px
    left:0
    right :0
    bottom :0
    background :#eee
    z-index :1
    .search-item
     line-height : 28px
     padding-left : 25px
     color :#666
     background :#fff 
     border-bottom :1px solid #666 
</style>
>>>>>>> city-search-logic
