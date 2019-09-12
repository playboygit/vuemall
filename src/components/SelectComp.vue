<template>
  <div class="select-comp">
    <span class="cur-select-btn" @click="ifShowList">
      <span>{{curPageTab}}</span>
      <em></em>   
    </span>
    <ul class="lm-list" v-show="ifShowTileList">
      <li v-for="(name, index) in navTabArr" :key="index" @click="switchPage(name)">{{name}}</li>
    </ul> 
  </div>
</template>

<script>
export default {
  name: 'SelectComp',
  data() {
    return {
      curPageTab:'首页',
      navTabArr: ['首页', '沸点', '活动'],
      ifShowTileList: false
    }
  },
  methods: {
    ifShowList() {
      this.ifShowTileList = !this.ifShowTileList
    },
    switchPage(name) {
      this.curPageTab = name
      this.ifShowList()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .select-comp {
    display: inline-block;
    vertical-align: middle;
    position: relative;
    .cur-select-btn {
      display: inline-block;
      font-size: 1.1429rem;
      padding-left: 0.2857rem;
      padding-right: 1.5429rem;
      color: #007fff;
      position: relative;
      em{
        display: inline-block;
        position: absolute;
        border: 0.4286rem solid transparent;
        border-top-color: #007fff;
        margin-top: 0.1429rem;
        top: 50%;
        transform: translate(0, -50%);
        right: 0.2857rem;
      }
    }
    .lm-list{
        position: absolute;
        top: 100%;
        left: 0;
        border:1px solid #ddd;
        border-radius: 0.2857rem;
        background-color: #fff;
        li{
          height: 3.5714rem;
          line-height: 3.5714rem;
          text-align: center;
          width: 4.2857rem;
          color: #999;
          .selected{
            color:#007fff;
          }
        }
      }
  }
</style>
