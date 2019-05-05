<template>
  <div class="rankingDescList">

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
  onShow () {
    console.log(this.$root.$mp.query.rankingType)
  },
  data () {
    return {
      bookList: [
        {
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1012797863/180',
          name: '电影世界私人订制',
          desc: '星海漫游，时空穿梭，机械科技，目标是未知的星辰大海！',
          author: '昨夜大雨',
          classification: '时空穿梭',
          state: '连载',
          fraction: '8.7'
        },
        {
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1012237441/180',
          name: '全球高武',
          desc: '重生过去、畅想未来、梦幻现实，再塑传奇人生！',
          author: '老鹰吃小鸡',
          classification: '修仙',
          state: '连载',
          fraction: '4.5'
        },
        {
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1010868264/180',
          name: '诡秘之主',
          desc: '心潮澎湃，无限幻想，迎风挥击千层浪，少年不败热血！',
          author: '爱潜水的乌贼',
          classification: '异世大陆',
          state: '连载',
          fraction: '9.2'
        },
        {
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1012982353/180',
          name: '史上最强赘婿',
          desc: '练武是不可能练武的，这辈子都不可能练武，只能靠吃软饭才能维持生活！',
          author: '沉默的糕点',
          classification: '东方玄幻',
          state: '连载',
          fraction: '8.5'
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
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1013561350/180',
          name: '仙宫',
          desc: '修仙觅长生，热血任逍遥，踏莲曳波涤剑骨，凭虚御风塑圣魂',
          author: '打眼',
          classification: '修仙',
          state: '连载',
          fraction: '4.6'
        },
        {
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1014234529/180',
          name: '我夺舍了魔皇',
          desc: '心潮澎湃，无限幻想，迎风挥击千层浪，少年不败热血！',
          author: '八月飞鹰',
          classification: '异世',
          state: '连载',
          fraction: '4.5'
        },
        {
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1013864366/180',
          name: '我和二哈共系统',
          desc: '心潮澎湃，无限幻想，迎风挥击千层浪，少年不败热血',
          author: '玄雨',
          classification: '玄幻',
          state: '连载',
          fraction: '4.5'
        },
        {
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1014151062/180',
          name: '抢救大明朝',
          desc: '醒掌天下权，醉卧美人膝，五千年风华烟雨，是非成败转头空！',
          author: '大罗罗',
          classification: '历史',
          state: '连载',
          fraction: '4.5'
        }
      ]
    }
  },
  computed: {

  },
  methods: {

  }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
