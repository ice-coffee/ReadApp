<template>
  <div class="shuchuang">

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

    <!--icon-->
    <div class="home_icon">
      <navigator url="/pages/ranking/main">
        <div class="icon_rank">
          <img src="/static/images/ic_ranking.png">
          <span>排行榜</span>
        </div>
      </navigator>
      <navigator url="/pages/classification/main">
        <div class="icon_classification">
          <img src="/static/images/ic_classification.png">
          <span>分类</span>
        </div>
      </navigator>
      <navigator url="/pages/free/main">
        <div class="icon_project">
          <img src="/static/images/ic_free_book.png">
          <span>免费</span>
        </div>
      </navigator>
      <navigator url="/pages/end/main">
        <div class="icon_project">
          <img src="/static/images/ic_end_book.png">
          <span>全本</span>
        </div>
      </navigator>
    </div>

    <!--热门连载-->
    <div>
      <div class="bookType" v-for="(item, index) in bookTypes" :key="index">
        <div class="head">
          {{item.title}}
          <span class="more">更多 ></span>
        </div>
        <div class="book_list" v-for="(bookItem, bookIndex) in item.bookList" :key="bookIndex">
          <img class="book_img" :src="bookItem.image"/>
          <div class="book_content">
            <p class="title">{{bookItem.name}}</p>
            <p class="introduction">{{bookItem.desc}}</p>
            <div class="desc">
              <div>
                <img src="/static/images/ic_book_auther.png"/>
                <span class="auther">{{bookItem.author}}</span>
              </div>
              <div class="descText">
                <span class="state">{{bookItem.fraction}}</span>
                <span class="state">{{bookItem.classification}}</span>
                <span class="state">{{bookItem.state}}</span>
              </div>
            </div>
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
      banner: [
        {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/7d3f40051a1ee5d94c7c908456d0ef10.jpg'},
        {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/cb30cc17b91772f23adfded87c4f353d.jpg'},
        {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/90e41d6449b0353c69b90d83e836feef.jpg'},
        {bannerImage: 'https://bossaudioandcomic-1252317822.file.myqcloud.com/activity/document/b9f3fa69b08413e97c19afab962fb2e5.jpg'}
      ],
      icon: [
        {}
      ],
      bookTypes: [
        {
          title: '热门连载',
          bookList: [
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1013926412/180',
              name: '暗月纪元',
              desc: '星海漫游，时空穿梭，机械科技，目标是未知的星辰大海！',
              author: '仐三',
              classification: '科幻',
              state: '连载',
              fraction: '4.5'
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
        },
        {
          title: '畅销精选',
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
            }
          ]
        },
        {
          title: '大神推荐',
          bookList: [
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
        },
        {
          title: '经典完本',
          bookList: [
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/3439785/180',
              name: '修真四万年',
              desc: '星海漫游，时空穿梭，机械科技，目标是未知的星辰大海！',
              author: '卧牛真人',
              classification: '未来世界',
              state: '完结',
              fraction: '9.2'
            },
            {
              image: 'https://bookcover.yuewen.com/qdbimg/349573/1209977/180',
              name: '斗破苍穹',
              desc: '这里是属于斗气的世界，没有花俏艳丽的魔法，有的，仅仅是繁衍到巅峰的斗气！',
              author: '天蚕土豆',
              classification: '异世大陆',
              state: '完结',
              fraction: '8.8'
            },
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
              image: 'https://bookcover.yuewen.com/qdbimg/349573/3660695/180',
              name: '神藏',
              desc: '重生过去、畅想未来、梦幻现实，再塑传奇人生！',
              author: '打眼',
              classification: '都市生活',
              state: '完结',
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

