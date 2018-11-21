<template>
  <!-- <div class="counter-warp">
    <p>Vuex counter：{{ count }}</p>
    <p>
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
    </p>
  </div> -->
  <div class="bt">
    <div class="bt-title">我的书架</div>
    <div class="bt-content">
      <div class="bt-list" v-for="item in bookList" :key="item.id" @click="navto">
        <img class="btl-img" :src="item.imgUrl" mode="widthFix" alt="">
        <div class="btl-desc">{{item.desc}}</div>
      </div>
    </div>
  </div>
</template>

<script>
// Use Vuex
// import store from './store'

export default {
  data () {
    return {
      bookList: [{
        id: 1,
        imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3677854586,3916838952&fm=26&gp=0.jpg',
        desc: '斗破苍穹'
      },
      {
        id: 2,
        imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3677854586,3916838952&fm=26&gp=0.jpg',
        desc: '斗破苍穹'
      },
      {
        id: 3,
        imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3677854586,3916838952&fm=26&gp=0.jpg',
        desc: '斗破苍穹'
      },
      {
        id: 4,
        imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3677854586,3916838952&fm=26&gp=0.jpg',
        desc: '斗破苍穹'
      }]
    }
  },
  computed: {
  },
  methods: {
    navto () {
      const url = '../bookBrowse/main'
      wx.navigateTo({ url })
    }
  }
}
</script>

<style lang="stylus" scoped rel="stylesheet/stylus">
.bt
  .bt-title
    font-size 28rpx
    color #333
    font-weight bolder
    padding-left 30rpx
  .bt-content
    display flex
    width 100%
    flex-wrap wrap
    .bt-list
      width 210rpx
      margin 30rpx 0 0 30rpx
      // background gray
      .btl-img
        width 210rpx
      .btl-desc
        font-size 24rpx
        line-height 50rpx
        color gray
        text-align center
</style>
