<template lang="html">
  <div class="icons">
    <swiper>
      <!-- slides -->
      <swiper-slide v-for="(page, index) in pages" :key="index">
        <div class="icon" v-for="item in page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.img" alt="">
          </div>
          <p class="icon-desc">{{item.text}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>

  </div>
</template>

<script>
export default {
  name: 'Icons',
  data () {
    return {
      iconListLeft: [
        {
          id: '001',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          text: '景点门票'
        }, {
          id: '002',
          img: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          text: '必游榜单'
        }, {
          id: '003',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
          text: '踏青赏花'
        }, {
          id: '004',
          img: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          text: '一日游'
        }, {
          id: '005',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          text: '动植物园'
        }, {
          id: '006',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
          text: '故宫'
        }, {
          id: '007',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png',
          text: '古北水镇'
        }, {
          id: '008',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/fa/fe1915e1d20bcc02.png',
          text: '定制游'
        }, {
          id: '009',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
          text: '演出'
        }, {
          id: '010',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
          text: '自然风光'
        }, {
          id: '011',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
          text: '名胜古迹'
        }, {
          id: '012',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/dd/cce1231836f10a02.png',
          text: '周边游'
        }, {
          id: '013',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
          text: '城市观光'
        }, {
          id: '014',
          img: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
          text: '游乐场'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconListLeft.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
  .icons
    overflow: hidden
    height: 0
    padding-bottom: 50%
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: .44rem
        box-sizing: border-box
        padding: .1rem
        .icon-img-content
          height: 100%
          display: block
          margin: 0 auto
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center
        color: $darkTextColor
        ellipsis()
</style>
