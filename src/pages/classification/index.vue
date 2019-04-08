<template>
  <div class="classification">

    <div class="classItem" v-for="(item, index) in classIficationList" :key="index">
      <div class="itemTitle">
        <span>{{item.className}}</span>
      </div>
      <div class="itemDesc">
        <span>{{item.classDesc}}</span>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  data () {
    return {
      classIficationList: [
        {
          className: '都市',
          classDesc: '生活 / 异能 / 重生 / 热血 / 人生'
        },
        {
          className: '玄幻',
          classDesc: '东方玄幻 / 异界大陆 / 转世重生'
        },
        {
          className: '仙侠',
          classDesc: '现代修真 / 奇幻修真 / 洪荒封神'
        },
        {
          className: '游戏',
          classDesc: '虚拟网游 / 游戏异界 / 游戏人生'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
