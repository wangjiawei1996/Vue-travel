<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.id"
        >
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/48/481516ec11298b7ba3.water.jpg_150x150_eff3aba2.jpg',
        title: '兰州极地海洋世界',
        desc: '年终Top1的排名，值得一玩'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/48/481516ec11298b7ba3.water.jpg_150x150_eff3aba2.jpg',
        title: '兰州极地海洋世界',
        desc: '年终Top1的排名，值得一玩'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/48/481516ec11298b7ba3.water.jpg_150x150_eff3aba2.jpg',
        title: '兰州极地海洋世界',
        desc: '年终Top1的排名，值得一玩'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      height: 1.7rem
      width: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
