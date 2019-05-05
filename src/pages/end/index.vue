<template>
  <div>

    <!--轮播-->
    <div class="freeBanner">
      <swiper autoplay="true" interval="3000" duration="500" circular="true">
        <block v-for="(item, index) in banner" :key="index">
          <swiper-item>
            <img :src="item.bannerImage" class="slide-image" />
          </swiper-item>
        </block>
      </swiper>
    </div>

    <!--分类推荐-->
    <div class="newBooks">
      <div v-for="(item, index) in classificationRecommendList" :key="index">
        <div class="title">
          <span>{{item.title}}</span>
        </div>
        <div class="bookList" v-for="(recommendBooks, bookIndex) in item.books" :key="bookIndex">
          <navigator>
            <img class="bookImage" :src="recommendBooks.image" />
            <div class="bookDesc">
              <span>{{recommendBooks.name}}</span>
              <span>{{recommendBooks.author}}/{{recommendBooks.classification}}/{{recommendBooks.state}}/{{recommendBooks.fraction}}</span>
              <span>{{recommendBooks.bookIntro}}</span>
            </div>
          </navigator>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  data () {
    return {
      banner: [
        {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/cb30cc17b91772f23adfded87c4f353d.jpg'},
        {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/b9f3fa69b08413e97c19afab962fb2e5.jpg'}
      ],
      classificationRecommendList: [
        {
          title: '新书精选',
          books: [
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1014151062/180',
              name: '抢救大明朝',
              desc: '醒掌天下权，醉卧美人膝，五千年风华烟雨，是非成败转头空！',
              author: '大罗罗',
              classification: '历史',
              state: '连载',
              fraction: '4.5'
            },
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1009704712/180',
              name: '牧神记',
              desc: '大墟的祖训说，天黑，别出门。',
              author: '宅猪',
              classification: '东方玄幻',
              state: '连载',
              fraction: '9.1'
            },
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1012237441/180',
              name: '全球高武',
              desc: '重生过去、畅想未来、梦幻现实，再塑传奇人生！',
              author: '老鹰吃小鸡',
              classification: '修仙',
              state: '连载',
              fraction: '4.5'
            }
          ]
        },
        {
          title: '新书精选',
          books: [
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1011058239/180',
              name: '伏天氏',
              desc: '心潮澎湃，无限幻想，迎风挥击千层浪，少年不败热血！',
              author: '净无痕',
              classification: '东方玄幻',
              state: '连载',
              fraction: '9.1'
            },
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1009480992/180',
              name: '超神机械师',
              desc: '肆意挥洒激情的游戏人生，打破现实框架的无尽幻想！',
              author: '齐佩甲',
              classification: '游戏异界',
              state: '连载',
              fraction: '9.0'
            },
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1010868264/180',
              name: '诡秘之主',
              desc: '心潮澎湃，无限幻想，迎风挥击千层浪，少年不败热血！',
              author: '爱潜水的乌贼',
              classification: '异世大陆',
              state: '连载',
              fraction: '9.2'
            }
          ]},
        {
          title: '新书精选',
          books: [
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1623837/180',
              name: '黄金瞳',
              desc: '重生过去、畅想未来、梦幻现实，再塑传奇人生！',
              author: '打眼',
              classification: '都市生活',
              state: '完结',
              fraction: '9.0'
            },
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1011486666/180',
              name: '大医凌然',
              desc: '医学院学生凌然有一个小目标，要成为世界上最伟大的医生，结果不小心实现了。',
              author: '志鸟村',
              classification: '都市生活',
              state: '连载',
              fraction: '9.0'
            },
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1011694114/180',
              name: '我的大明新帝国',
              desc: '醒掌天下权，醉卧美人膝，五千年风华烟雨，是非成败转头空！',
              author: '摇摇-欲坠',
              classification: '历史',
              state: '完结',
              fraction: '8.6'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
