<template>
  <div class="navBlock">
    <div class="navtop">
      <img :src="logo" class="nav-logo">
      <div class="m-nav-lm-list">
        <SelectComp></SelectComp>     
      </div>
      <SearchIpt></SearchIpt>
      <div class="login-group-box">
        <a href="javascript:;">登录</a>
        <span>.</span>
        <a href="javascript:;">注册</a>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '../assets/logo.png'
import SelectComp from '@/components/SelectComp.vue'
import SearchIpt from '@/components/SearchIpt.vue'
export default {
  name: 'navBlock',
  data() {
    return {
      logo:Logo
    }
  },
  components:{
    SelectComp,
    SearchIpt
  },
  methods: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
$navHeight:4.2857rem;
.navtop{
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: $navHeight;
  line-height: $navHeight;
  border-bottom: 1px solid #ddd;
  background-color: #fff;
  z-index:1000;
  .m-nav-lm-list{
    display: inline-block;
    line-height: $navHeight;
    margin-left: 0.4286rem;
  }
  .login-group-box{
    height: $navHeight;
    line-height: $navHeight;
    padding-right: 0.4286rem;
    text-align: right;
    position: absolute;
    right: 0;
    top: 0;
    a{
      color: #007fff;
    }
    span{
      display: inline-block;
      color: #007fff;
      font-size: 1.4286rem;
      margin: 0 0.1429rem;
      vertical-align: 0.1429rem
    }
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
