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
          rankCover: 'https://bookcover.yuewen.com/qdbimg/349573/1010868264/180',
          rankTitle: '人气榜'
        },
        {
          rankCover: 'https://bookcover.yuewen.com/qdbimg/349573/1010734492/180',
          rankTitle: '原创榜'
        },
        {
          rankCover: 'https://bookcover.yuewen.com/qdbimg/349573/1009704712/180',
          rankTitle: '完结榜'
        },
        {
          rankCover: 'https://bookcover.yuewen.com/qdbimg/349573/1013926412/180',
          rankTitle: '新书榜'
        },
        {
          rankCover: 'https://bookcover.yuewen.com/qdbimg/349573/1014151062/180',
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
