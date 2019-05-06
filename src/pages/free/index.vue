<template>
  <div>

    <!--轮播-->
    <div class="freeBanner">
      <swiper autoplay="true" interval="3000" duration="500" circular="true">
        <block v-for="(item, index) in banner" :key="index">
          <swiper-item>
            <img :src="item.bannerImage" class="slide-image" />
          </swiper-item>
        </block>
      </swiper>
    </div>

    <!--限时免费-->
    <div class="timeFree">
      <div class="title">
        <span>限时免费</span>
      </div>
      <div class="bookList">
        <div v-for="(item, index) in timeFreeBooks" :key="index">
          <navigator :url="'/pages/bookdetails/main?bookId=' + item.id">
            <img class="bookImage" :src="item.image" />
            <span>{{item.name}}</span>
          </navigator>
        </div>
      </div>
    </div>

    <!--分类推荐-->
    <div class="newBooks">
      <div v-for="(item, index) in classificationRecommendList" :key="index">
        <div class="title">
          <span>{{item.title}}</span>
        </div>
        <div class="bookList" v-for="(recommendBooks, bookIndex) in item.books" :key="bookIndex">
          <navigator :url="'/pages/bookdetails/main?bookId=' + recommendBooks.id">
            <img class="bookImage" :src="recommendBooks.image" />
            <div class="bookDesc">
              <span>{{recommendBooks.name}}</span>
              <span>{{recommendBooks.author}}/{{recommendBooks.classification}}/{{recommendBooks.state}}/{{recommendBooks.fraction}}</span>
              <span>{{recommendBooks.bookIntro}}</span>
            </div>
          </navigator>
        </div>
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
          {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/cb30cc17b91772f23adfded87c4f353d.jpg'}
        ],
        timeFreeBooks: books.slice(0, 8),
        classificationRecommendList: [
          {
            title: '新书精选',
            books: books.slice(0, 4)
          },
          {
            title: '新书榜',
            books: books.slice(4, 8)
          },
          {
            title: '名家推荐',
            books: books.slice(8, 12)
          }
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
