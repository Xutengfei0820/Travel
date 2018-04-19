<template lang="html">
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
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
        id: '01',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/10/b892e5069c3508f7b017a91121502223.jpg_200x200_3d7db4ec.jpg',
        title: '古北水镇',
        desc: '长城脚下独具北方风情的度假式小镇'
      }, {
        id: '02',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/10/b892e5069c3508f7b017a91121502223.jpg_200x200_3d7db4ec.jpg',
        title: '古北水镇',
        desc: '长城脚下独具北方风情的度假式小镇'
      }, {
        id: '03',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/10/b892e5069c3508f7b017a91121502223.jpg_200x200_3d7db4ec.jpg',
        title: '古北水镇',
        desc: '长城脚下独具北方风情的度假式小镇'
      }, {
        id: '04',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/10/b892e5069c3508f7b017a91121502223.jpg_200x200_3d7db4ec.jpg',
        title: '古北水镇',
        desc: '长城脚下独具北方风情的度假式小镇'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
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
        line-height: .46rem
        margin-top: .2rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
