<template>
  <div class="bookcase">

    <!--搜索-->
    <div class="home_search">
      <div>
        <img class="icon" src="/static/images/ic_search.png"/>
      </div>
      <div class="input">
        <input type="text" placeholder="书名/作者"/>
      </div>
    </div>

    <!--轮播图-->
    <div class="home_banner">
      <swiper autoplay="true" interval="3000" duration="500" circular="true">
        <block v-for="(item, index) in banner" :key="index">
          <swiper-item>
            <img :src="item.bannerImage" class="slide-image" />
          </swiper-item>
        </block>
      </swiper>
    </div>

    <!--icon-->
    <div class="home_icon">
      <div class="icon_rank">
        <img src="/static/images/ic_ranking.png">
        <span>排行榜</span>
      </div>
      <div class="icon_classification">
        <img src="/static/images/ic_classification.png">
        <span>分类</span>
      </div>
      <div class="icon_project">
        <img src="/static/images/ic_project.png">
        <span>专题</span>
      </div>
    </div>

    <!--热门连载-->
    <div class="hotbook">
      <div class="head">
        {{hotBooks.title}}
        <span class="more">更多 ></span>
      </div>
      <div class="book_list" v-for="(item, index) in hotBooks.bookList" :key="index">
        <img class="book_img" :src="item.image"/>
        <div class="book_content">
          <p class="title">{{item.name}}</p>
          <p class="desc">{{item.desc}}</p>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  data () {
    return {
      banner: [
        {bannerImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg'},
        {bannerImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg'},
        {bannerImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg'},
        {bannerImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg'}
      ],
      icon: [
        {}
      ],
      hotBooks: {
        title: '热门连载',
        bookList: [
          {
            image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
            name: '妹子,我教你修仙',
            desc: '妹子,你有房吗'
          },
          {
            image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
            name: '妹子,我教你修仙',
            desc: '妹子,你有房吗'
          },
          {
            image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
            name: '妹子,我教你修仙',
            desc: '妹子,你有房吗'
          },
          {
            image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
            name: '妹子,我教你修仙',
            desc: '妹子,你有房吗'
          },
          {
            image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
            name: '妹子,我教你修仙',
            desc: '妹子,你有房吗'
          }
        ]
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>

