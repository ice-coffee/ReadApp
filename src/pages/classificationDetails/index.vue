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
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1014151062/180',
          name: '抢救大明朝',
          desc: '醒掌天下权，醉卧美人膝，五千年风华烟雨，是非成败转头空！',
          author: '大罗罗',
          classification: '历史',
          state: '连载',
          fraction: '4.5'
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
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1010734492/180',
          name: '凡人修仙之仙界篇',
          desc: '修仙觅长生，热血任逍遥，踏莲曳波涤剑骨，凭虚御风塑圣魂！',
          author: '忘语',
          classification: '仙侠',
          state: '连载',
          fraction: '9.0'
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
          image: 'https://bookcover.yuewen.com/qdbimg/349573/1011705052/180',
          name: '明朝败家子',
          desc: '醒掌天下权，醉卧美人膝，五千年风华烟雨，是非成败转头空！',
          author: '上山打老虎额',
          classification: '历史',
          state: '连载',
          fraction: '9.0'
        },
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
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
