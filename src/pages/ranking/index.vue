<template>
  <div class="ranking">

    <div v-for="(item, index) in rankList" :key="index">
      <navigator url="/pages/rankingDesc/main?rankingType=0">
        <div class="item">
          <img class="itemCover" :src="item.rankCover"/>
          <span class="itemName">{{item.rankTitle}}</span>
          <img class="itemArrow" src="/static/images/ic_arrow_right.png"/>
        </div>
      </navigator>
    </div>

  </div>
</template>

<script>
export default {
  data () {
    return {
      rankList: [
        {
          rankCover: '/static/images/bg_rank_cover.png',
          rankTitle: '人气榜'
        },
        {
          rankCover: '/static/images/bg_rank_cover.png',
          rankTitle: '原创榜'
        },
        {
          rankCover: '/static/images/bg_rank_cover.png',
          rankTitle: '完结榜'
        },
        {
          rankCover: '/static/images/bg_rank_cover.png',
          rankTitle: '新书榜'
        },
        {
          rankCover: '/static/images/bg_rank_cover.png',
          rankTitle: '书友推荐榜'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
