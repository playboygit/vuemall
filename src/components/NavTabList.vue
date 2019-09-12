<template>
  <div class="nav-tab-list-box">
    <ul class="nav-tab-list">
      <router-link :to="{path: '/'+item.type}" tag="li" v-for="(item, index) in navList" :key="index">
        <span>{{item.name}}</span>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'NavTabList',
  data() {
    return {
      navList: [
        {
          name: '推荐',
          type: 'recommend'
        },
        {
          name: '后端',
          type: 'backend'
        },
        {
          name: '前端',
          type: 'fontend'
        },
        {
          name: 'Android',
          type: 'android'
        },
        {
          name: 'IOS',
          type: 'ios'
        },
        {
          name: '人工智能',
          type: 'ai'
        },
        {
          name: '大数据',
          type: 'bigdata'
        },
        {
          name: '区块链',
          type: 'blockchain'
        }
      ]
    }
  },
  components:{
    
  },
  mounted () {
    
  },
  methods: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
$navHeight:4.2857rem;
.nav-tab-list-box{
  position: fixed;
  top: 4.2857rem;
  left: 0;
  width: 100vw;
  background-color: #fff;
  z-index:999;
}
.nav-tab-list{
  display: flex;
  align-items: center;
  width:auto;
  overflow: hidden;
  overflow-x: auto;
  box-shadow: 0 1px 2px 0 rgba(0,0,0,.05);
  li{
    display: flex;
    height: 2.8571rem;
    line-height: 2.8571rem;
    padding:0 0.7143rem;
    text-align: center;
    color: #666;
    white-space: nowrap;
  }
  .router-link-active{
    color: #007fff;
  }
}
.nav-logo{
  width: 2.8571rem;
  height: 2.8571rem;
  margin-left: 0.7143rem;
  display: inline-block;
  vertical-align: middle;
}
</style>
