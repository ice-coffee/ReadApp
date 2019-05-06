<template>
  <div class="rankingDescList">

    <div class="bookList" v-for="(item, index) in bookList" :key="index">
      <img class="bookImage" :src="item.image"/>
      <div class="bookContent">
        <div class="bookName">{{item.name}}</div>
        <div class="bookDesc">{{item.desc}}</div>
      </div>
      <img class="bookEdit" src="/static/images/ic_book_auther.png"/>
    </div>

  </div>
</template>

<script>
  import books from '../../utils/books'

  export default {
    onShow () {
      this.rankingType = this.$root.$mp.query.rankingType
      this.bookList = books.slice((0 + this.rankingType * 2), (5 + this.rankingType * 2))
    },
    data () {
      return {
        rankingType: 0,
        bookList: []
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
