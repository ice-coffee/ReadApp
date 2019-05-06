<template>
  <div class="shuchuang">

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
          <img src="/static/images/ic_free_book.png">
          <span>免费</span>
        </div>
      </navigator>
      <navigator url="/pages/end/main">
        <div class="icon_project">
          <img src="/static/images/ic_end_book.png">
          <span>全本</span>
        </div>
      </navigator>
    </div>

    <!--热门连载-->
    <div>
      <div class="bookType" v-for="(item, index) in bookTypes" :key="index">
        <div class="head">
          {{item.title}}
        </div>
        <navigator :url="'/pages/bookdetails/main?bookId=' + bookItem.id" class="book_list" v-for="(bookItem, bookIndex) in item.bookList" :key="bookIndex">
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
        </navigator>
      </div>
    </div>

  </div>
</template>

<script>
  import books from '../../utils/books'

  export default {
    data () {
      return {
        banner: [
          {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/7d3f40051a1ee5d94c7c908456d0ef10.jpg'},
          {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/cb30cc17b91772f23adfded87c4f353d.jpg'},
          {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/90e41d6449b0353c69b90d83e836feef.jpg'},
          {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/b9f3fa69b08413e97c19afab962fb2e5.jpg'}
        ],
        icon: [
          {}
        ],
        bookTypes: [
          {
            title: '热门连载',
            bookList: books.slice(0, 5)
          },
          {
            title: '畅销精选',
            bookList: books.slice(5, 10)
          },
          {
            title: '大神推荐',
            bookList: books.slice(10, 15)
          },
          {
            title: '经典完本',
            bookList: books.slice(15, 20)
          }
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>

