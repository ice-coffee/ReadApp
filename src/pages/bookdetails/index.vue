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
  export default {
    data () {
      return {
        bookDetails: {
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1013926412/180',
          name: '暗月纪元',
          desc: '星海漫游，时空穿梭，机械科技，目标是未知的星辰大海！',
          author: '仐三',
          classification: '科幻',
          state: '连载',
          fraction: '4.5'
        }
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
