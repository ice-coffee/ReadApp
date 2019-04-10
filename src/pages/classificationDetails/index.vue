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
export default {
  data () {
    return {
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
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
