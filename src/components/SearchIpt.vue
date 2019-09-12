<template>
  <div class="search-ipt">
    <input type="text" placeholder="搜索...">
  </div>
</template>

<script>
export default {
  name: 'SelectIpt'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .search-ipt {
    display: inline-block;
    vertical-align: middle;
    width: 10rem;
    margin-left: 1rem;
    input{
        width: 100%;
        height: 2.2571rem;
        border:1px solid #ddd;
        background-color: #fefefe;
        padding:0 0.2857rem;
        border-radius: 0.1429rem;
    }
    input:focus{
        background-color: #fff;
        border-color: #007fff;
    }
  }
</style>
