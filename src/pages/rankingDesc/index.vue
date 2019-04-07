<template>
  <div>
    <span>排行详情</span>
  </div>
</template>

<script>
export default {
  onShow () {
    console.log(this.$root.$mp.query.rankingType)
  },
  data () {
    return {

    }
  }

}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
