<template>
  <div class="bookCase">

    <div class="bookList" v-for="(item, index) in bookList" :key="index">
      <img class="bookImage" :src="item.image"/>
      <div class="bookContent">
        <div class="bookName">{{item.name}}</div>
        <div class="bookDesc">{{item.desc}}</div>
      </div>
    </div>

  </div>
</template>

<script>
  import books from '../../utils/books'

  export default {
    data () {
      return {
        bookList: books
      }
    },
    onShow () {
      wx.setStorageSync('logs', JSON.stringify(books.slice(0, 5)))
      this.bookList = JSON.parse(wx.getStorageSync('logs'))
    }
  }
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
