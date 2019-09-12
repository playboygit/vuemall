<template>
  <div class="recommend">
      <ul class="recommend-list">
            <li v-for="(item, index) in recommendList" :key="index">
                <RecommendItem :recommendObj="item"></RecommendItem>    
            </li>
      </ul>
  </div>
</template>

<script>
import RecommendItem from '@/components/RecommendItem.vue'

export default {
  name: 'recommend',
  data() {
        return {
            recommendList: [
                {
                    specialName:'专栏',
                    author: 'kenbliky',
                    time: '10分钟前',
                    column: '机器学习',
                    titleName: 'python 科学计算的基石，快来学习吧（一）',
                    thumbsupNum: 102,
                    replyNum: 12
                },
                {
                    specialName:'专栏',
                    author: 'kenbliky',
                    time: '10分钟前',
                    column: '机器学习',
                    titleName: 'python 科学计算的基石，快来学习吧（一）',
                    thumbsupNum: 101,
                    replyNum: 12
                },
                {
                    specialName:'专栏',
                    author: 'kenbliky',
                    time: '10分钟前',
                    column: '机器学习',
                    titleName: 'python 科学计算的基石，快来学习吧（一）',
                    thumbsupNum: 102,
                    replyNum: 12
                },
                {
                    specialName:'专栏',
                    author: 'kenbliky',
                    time: '10分钟前',
                    column: '机器学习',
                    titleName: 'python 科学计算的基石，快来学习吧（一）',
                    thumbsupNum: 101,
                    replyNum: 12
                },
                {
                    specialName:'专栏',
                    author: 'kenbliky',
                    time: '10分钟前',
                    column: '机器学习',
                    titleName: 'python 科学计算的基石，快来学习吧（一）',
                    thumbsupNum: 102,
                    replyNum: 12
                },
                {
                    specialName:'专栏',
                    author: 'kenbliky',
                    time: '10分钟前',
                    column: '机器学习',
                    titleName: 'python 科学计算的基石，快来学习吧（一）',
                    thumbsupNum: 101,
                    replyNum: 12
                },
                {
                    specialName:'专栏',
                    author: 'kenbliky',
                    time: '10分钟前',
                    column: '机器学习',
                    titleName: 'python 科学计算的基石，快来学习吧（一）',
                    thumbsupNum: 102,
                    replyNum: 12
                },
                {
                    specialName:'专栏',
                    author: 'kenbliky',
                    time: '10分钟前',
                    column: '机器学习',
                    titleName: 'python 科学计算的基石，快来学习吧（一）',
                    thumbsupNum: 101,
                    replyNum: 12
                }
            ]
        }
  },
  components: {
    RecommendItem
  },
  mounted () {
    this.$http.get().then((response) => {
        console.log(response)
    })  
  },
  methods: {
    
  }
}
</script>
<style scoped lang="scss">
.recommend-list{
    background-color: #fff;
    li{
        border-bottom: 1px solid #eee;
    }
    li:last{
        border-bottom: none;
    }
}
</style>
