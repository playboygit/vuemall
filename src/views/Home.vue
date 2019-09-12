<template>
  <div class="home">
    <nav class="page-nav">
      <NavBlock></NavBlock>
      <NavTabList></NavTabList>
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
// @ is an alias to /src
import NavBlock from "@/components/NavBlock.vue"
import NavTabList from "@/components/NavTabList.vue"

export default {
  name: "home",
  components: {
    NavBlock,
    NavTabList
  },
  methods: {},
  mounted() {
    
  },
}
</script>
<style scoped lang="scss">
.page-nav{
  height: 7.1429rem;
}
</style>
