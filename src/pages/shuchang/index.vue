<template>
  <div class="shuchuang">

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
      <navigator url="/pages/ranking/main">
        <div class="icon_rank">
          <img src="/static/images/ic_ranking.png">
          <span>排行榜</span>
        </div>
      </navigator>
      <navigator url="/pages/classification/main">
        <div class="icon_classification">
          <img src="/static/images/ic_classification.png">
          <span>分类</span>
        </div>
      </navigator>
      <navigator url="/pages/free/main">
        <div class="icon_project">
          <img src="/static/images/ic_project.png">
          <span>免费</span>
        </div>
      </navigator>
      <navigator>
        <div class="icon_project">
          <img src="/static/images/ic_project.png">
          <span>全本</span>
        </div>
      </navigator>
    </div>

    <!--热门连载-->
    <div>
      <div class="bookType" v-for="(item, index) in bookTypes" :key="index">
        <div class="head">
          {{item.title}}
          <span class="more">更多 ></span>
        </div>
        <div class="book_list" v-for="(bookItem, bookIndex) in item.bookList" :key="bookIndex">
          <img class="book_img" :src="bookItem.image"/>
          <div class="book_content">
            <p class="title">{{bookItem.name}}</p>
            <p class="introduction">{{bookItem.desc}}</p>
            <div class="desc">
              <div>
                <img src="/static/images/ic_book_auther.png"/>
                <span class="auther">{{bookItem.author}}</span>
              </div>
              <div class="descText">
                <span class="state">{{bookItem.fraction}}</span>
                <span class="state">{{bookItem.classification}}</span>
                <span class="state">{{bookItem.state}}</span>
              </div>
            </div>
          </div>
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
      bookTypes: [
        {
          title: '热门连载',
          bookList: [
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            }
          ]
        },
        {
          title: '男生短片',
          bookList: [
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            }
          ]
        },
        {
          title: '大神推荐',
          bookList: [
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            }
          ]
        },
        {
          title: '经典完本',
          bookList: [
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
              name: '妹子,我教你修仙',
              desc: '妹子,你有房吗',
              author: '北极仙人',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>

