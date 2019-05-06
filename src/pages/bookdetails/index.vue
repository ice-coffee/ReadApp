<template>
  <div class="bookdetails">

    <div class="head">
      <img class="book_img" :src="bookDetails.image"/>
      <div class="book_content">
        <p class="title">{{bookDetails.name}}</p>
        <p class="fraction">{{bookDetails.fraction}}</p>
        <p class="classification">{{bookDetails.classification}}</p>
        <div class="bookauther">
          <img src="/static/images/ic_book_auther.png"/>
          <span class="auther">{{bookDetails.author}}</span>
        </div>
      </div>
    </div>

    <div class="bookstate">
      <div>
        <p class="statevalue">827</p>
        <p class="statekey">人气</p>
      </div>
      <div>
        <p class="statevalue">{{bookDetails.state}}</p>
        <p class="statekey">状态</p>
      </div>
      <div>
        <p class="statevalue">827</p>
        <p class="statekey">字数</p>
      </div>
    </div>

    <div class="introduction">
      <span class="title">简介</span>
      <p class="desc">{{bookDetails.desc}}</p>
    </div>
  </div>
</template>

<script>
  import books from '../../utils/books'

  export default {
    onShow () {
      let bookId = parseInt(this.$root.$mp.query.bookId)
      for (var i = 0; i < books.length; i++) {
        let book = books[i]
        if (book.id === bookId) {
          this.bookDetails = book
        }
      }
    },
    data () {
      return {
        bookDetails: []
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
