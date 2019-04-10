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

    <!--限时免费-->
    <div class="timeFree">
      <div class="title">
        <span>限时免费</span>
        <span>更多 ></span>
      </div>
      <div class="bookList">
        <div v-for="(item, index) in timeFreeBooks" :key="index">
          <navigator>
            <img class="bookImage" :src="item.bookImage" />
            <span>{{item.bookName}}</span>
          </navigator>
        </div>
      </div>
    </div>

    <!--新书精选-->
    <div class="newBooks">
      <div class="title">
        <span>新书精选</span>
        <span>更多 ></span>
      </div>
      <div class="bookList" v-for="(item, index) in newBooks" :key="index">
        <navigator>
          <img class="bookImage" :src="item.bookImage" />
          <div class="bookDesc">
            <span>{{item.bookName}}</span>
            <span>{{item.bookAuther}}/{{item.bookType}}/{{item.bookState}}/{{item.bookWordCount}}</span>
            <span>{{item.bookIntro}}</span>
          </div>
        </navigator>
      </div>
    </div>

    <!--科幻专场-->
    <div class="futureBooks">
      <div class="title">
        <span>科幻专场</span>
        <span>更多 ></span>
      </div>
      <div class="bookList" v-for="(item, index) in futrueBooks" :key="index">
        <navigator>
          <img class="bookImage" :src="item.bookImage" />
          <div class="bookDesc">
            <span>{{item.bookName}}</span>
            <span>{{item.bookAuther}}/{{item.bookType}}/{{item.bookState}}/{{item.bookWordCount}}</span>
            <span>{{item.bookIntro}}</span>
          </div>
        </navigator>
      </div>
    </div>


    <!--游戏专场-->
    <div class="gameBooks">
      <div class="title">
        <span>游戏专场</span>
        <span>更多 ></span>
      </div>
      <div class="bookList" v-for="(item, index) in newBooks" :key="index">
        <navigator>
          <img class="bookImage" :src="item.bookImage" />
          <div class="bookDesc">
            <span>{{item.bookName}}</span>
            <span>{{item.bookAuther}}/{{item.bookType}}/{{item.bookState}}/{{item.bookWordCount}}</span>
            <span>{{item.bookIntro}}</span>
          </div>
        </navigator>
      </div>
    </div>


  </div>
</template>

<script>
export default {
  data () {
    return {
      banner: [
        {bannerImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg'},
        {bannerImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg'},
        {bannerImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg'},
        {bannerImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg'}
      ],
      timeFreeBooks: [
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '凡人修仙传'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '凡人修仙传'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '凡人修仙传'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '凡人修仙传'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '凡人修仙传'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '凡人修仙传'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '凡人修仙传'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '凡人修仙传'
        }
      ],
      newBooks: [
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '暗月纪',
          bookAuther: '十三',
          bookType: '科幻',
          bookState: '连载',
          bookWordCount: '20万字',
          bookIntro: '紫月升起之夜,时代颠覆之时'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '暗月纪',
          bookAuther: '十三',
          bookType: '科幻',
          bookState: '连载',
          bookWordCount: '20万字',
          bookIntro: '紫月升起之夜,时代颠覆之时'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '暗月纪',
          bookAuther: '十三',
          bookType: '科幻',
          bookState: '连载',
          bookWordCount: '20万字',
          bookIntro: '紫月升起之夜,时代颠覆之时'
        }
      ],
      futrueBooks: [
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '我的专属梦境游戏',
          bookAuther: '碧蓝的世界',
          bookType: '科幻',
          bookState: '连载',
          bookWordCount: '30万字',
          bookIntro: '一个晚上能当半年用,还能从现实中复制一个角色'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '我的专属梦境游戏',
          bookAuther: '碧蓝的世界',
          bookType: '科幻',
          bookState: '连载',
          bookWordCount: '30万字',
          bookIntro: '一个晚上能当半年用,还能从现实中复制一个角色'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '我的专属梦境游戏',
          bookAuther: '碧蓝的世界',
          bookType: '科幻',
          bookState: '连载',
          bookWordCount: '30万字',
          bookIntro: '一个晚上能当半年用,还能从现实中复制一个角色'
        }
      ],
      gameBooks: [
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '游戏之金刚不坏',
          bookAuther: '铁牛仙',
          bookType: '游戏',
          bookState: '连载',
          bookWordCount: '40万字',
          bookIntro: '我从小被我爹打到大,他都没打死我何况你们?'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '游戏之金刚不坏',
          bookAuther: '铁牛仙',
          bookType: '游戏',
          bookState: '连载',
          bookWordCount: '40万字',
          bookIntro: '我从小被我爹打到大,他都没打死我何况你们?'
        },
        {
          bookImage: 'http://i0.hdslb.com/bfs/archive/ffe9735cdb517513b7de05d95767eef31abe3da9.jpg',
          bookName: '游戏之金刚不坏',
          bookAuther: '铁牛仙',
          bookType: '游戏',
          bookState: '连载',
          bookWordCount: '40万字',
          bookIntro: '我从小被我爹打到大,他都没打死我何况你们?'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "./style.scss";
</style>
