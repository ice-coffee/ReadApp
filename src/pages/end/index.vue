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

    <!--分类推荐-->
    <div class="newBooks">
      <div v-for="(item, index) in classificationRecommendList" :key="index">
        <div class="title">
          <span>{{item.title}}</span>
        </div>
        <div class="bookList" v-for="(recommendBooks, bookIndex) in item.books" :key="bookIndex">
          <navigator>
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
          {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/cb30cc17b91772f23adfded87c4f353d.jpg'},
          {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/b9f3fa69b08413e97c19afab962fb2e5.jpg'}
        ],
        classificationRecommendList: [
          {
            title: '新书精选',
            books: books.slice(4, 9)
          },
          {
            title: '新书精选',
            books: books.slice(9, 14)
          },
          {
            title: '新书精选',
            books: books.slice(14, 19)
          }
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
