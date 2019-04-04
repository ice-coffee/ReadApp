<template>
  <div class="bookcase">

    <!--搜索-->
    <div class="home_search">
      <div>
        <img class="icon" src="/static/images/ic_search.png"/>
      </div>
      <div class="input">
        <input type="text" placeholder="书名/作者"/>
      </div>
    </div>

    <!--轮播图-->
    <div class="home_banner">
      <swiper autoplay="true" interval="3000" duration="500" circular="true">
        <block v-for="(item, index) in banner" :key="index">
          <swiper-item>
            <img :src="item.bannerImage" class="slide-image" />
          </swiper-item>
        </block>
      </swiper>
    </div>

    <div class="home_icon">
      <div class="icon_rank">

      </div>
      <div class="icon_classification">

      </div>
      <div class="icon_">

      </div>
    </div>
  </div>
</template>

<script>

</script>

<style scoped>
  @import "./style.scss";
</style>
