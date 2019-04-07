<template>
  <div class="bookCase">

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
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
