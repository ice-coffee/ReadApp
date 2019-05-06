<template>
  <div class="classificationDestails">

    <div class="book_list" v-for="(item, index) in bookList" :key="index">
      <img class="book_img" :src="item.image"/>
      <div class="book_content">
        <p class="title">{{item.name}}</p>
        <p class="introduction">{{item.desc}}</p>
        <div class="desc">
          <div>
            <img src="/static/images/ic_book_auther.png"/>
            <span class="auther">{{item.author}}</span>
          </div>
          <div class="descText">
            <span class="state">{{item.fraction}}</span>
            <span class="state">{{item.classification}}</span>
            <span class="state">{{item.state}}</span>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
  import books from '../../utils/books'

  export default {
    onShow () {
      let type = this.$root.$mp.query.type
      this.bookList = books.slice((0 + type * 3), (5 + type * 3))
    },
    data () {
      return {
        bookList: []
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
