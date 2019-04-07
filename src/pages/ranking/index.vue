<template>
  <div>
    <div class="navbar">
      <block v-for="(item,index) in tabs" :key="index">
        <div :id="index" :class="{'navbar_item_on':activeIndex == index}" class="navbar_item" @click="tabClick">
          <div class="navbar_title">{{item.name}}</div>
        </div>
      </block>
      <div class="navbar_slider" :class="navbarSliderClass"></div>
    </div>
    <div>
      <div :hidden="activeIndex != 0">选项一的内容</div>
      <div :hidden="activeIndex != 1">选项二的内容</div>
      <div :hidden="activeIndex != 2">选项三的内容</div>
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        tabs: [
          {
            name: '选项卡1',
            type: '1',
            checked: true
          },
          {
            name: '选项卡2',
            type: '2',
            checked: true
          },
          {
            name: '选项卡3',
            type: '3',
            checked: true
          }
        ],
        activeIndex: 0
      }
    },
    computed: {
      navbarSliderClass: function () {
        if (this.activeIndex === 0) {
          console.log('1')
          return 'navbar_slider_0'
        } else if (this.activeIndex === 1) {
          console.log('2')
          return 'navbar_slider_1'
        } else if (this.activeIndex === 2) {
          console.log('3')
          return 'navbar_slider_2'
        }
      }
    },
    methods: {
      tabClick: function (e) {
        this.activeIndex = e.currentTarget.id
      }
    }
  }
</script>

<style lang="scsss" scoped>
  @import "./style.scss";
</style>
