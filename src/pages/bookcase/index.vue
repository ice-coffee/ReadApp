<template>
  <div class="bookCase">

    <navigator :url="'/pages/bookdetails/main?bookId=' + item.id" class="bookList" v-for="(item, index) in bookList" :key="index">
      <img class="bookImage" :src="item.image"/>
      <div class="bookContent">
        <div class="bookName">{{item.name}}</div>
        <div class="bookDesc">{{item.desc}}</div>
      </div>
    </navigator>

  </div>
</template>

<script>
  export default {
    onShow () {
      this.bookList = JSON.parse(wx.getStorageSync('books'))
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
