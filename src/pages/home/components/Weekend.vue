<template>
  <div>
    <div class="title">假期去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <div class="item-img-wrapper">
            <img class="item-img" :src="item.imgUrl"/>
          </div>
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
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1602/68/68aa05adb5315f9990.water.jpg_200x200_ce3d2658.jpg',
        title: '北京海洋馆',
        desc: '奇幻海洋之旅，在帝都感受大海的魅力！'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/2f/e615bc3c8e0cf46d9fb92c58ac305f45.water.jpg_200x200_e4e69a48.jpg',
        title: '世界公园',
        desc: ''
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/f5/f5f45e1a83537bcb.water.jpg_200x200_444cc7e8.jpg',
        title: '圆明园',
        desc: '百年皇家的珍宝，民族耻辱的见证'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  @import '~styles/varibles.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 4rem
    width: 100%
    .item-img
      width: 100%
      height: 4rem
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: $darkTextColor
      ellipsis()
</style>
