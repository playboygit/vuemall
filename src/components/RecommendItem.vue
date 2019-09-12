<template>
  <div class="recommend-item">
      <p class="small-title clip">
          <span class="special-type">{{recommendObj.specialName}}</span>
          <span class="normal-type">{{recommendObj.author}}</span>
          <span class="normal-type">{{recommendObj.time}}</span>
          <span class="normal-type nopoint">{{recommendObj.column}}</span>
      </p>
      <p class="item-title clip">{{recommendObj.titleName}}</p>
      <div class="item-btn-group">
            <ul class="btn-list">
                <li class="cl">
                    <img src="https://b-gold-cdn.xitu.io/v3/static/img/zan.e9d7698.svg" alt="">
                    <span>{{recommendObj.thumbsupNum}}</span>
                </li>
                <li>
                    <img src="https://b-gold-cdn.xitu.io/v3/static/img/comment.4d5744f.svg" alt="">
                    <span>{{recommendObj.replyNum}}</span>
                </li>
            </ul>
      </div>
  </div>
</template>

<script>

export default {
  name: 'RecommendItem',
  props: ['recommendObj'],
  data() {
        return {
            
        }
  },
  methods: {
    
  }
}
</script>
<style scoped lang="scss">
$stextcolor: #999;
.recommend-item{
    padding: 0.8571rem 1.4286rem;
    .small-title{
        font-size: 0.8571rem;
        span{
            display: inline-block;
            padding-right: 0.7143rem;
            position: relative;
            color: $stextcolor;
        }
        span:after{
            content: '.';
            position: absolute;
            font-size: 1.4429rem;
            color: $stextcolor;
            right: 0.1857rem;
            top: 50%;
            transform: translate(0, -50%);
            margin-top: -0.4143rem;
        }
        .nopoint:after{
            content: '';
        }
        .special-type{
            color: #b71ed7;
            font-weight: 500;
        }
        .middle-point{
            vertical-align: -0.1429rem;
            display: inline-block;
        }
    }
    .item-title{
        font-weight: 700;
        margin-top: 0.5714rem;
    }
    .item-btn-group{
        margin-top: 0.8571rem;
        .btn-list{
            border:1px solid #ddd;
            border-radius: 0.1429rem;
            display: inline-flex;
            width: auto;
            li{
                display: flex;
                padding: 0 0.5714rem;
                border-right: 1px solid #ddd;
                align-items: center;
                color: #b2bac2;
                font-weight: 700;
                font-size: 0.8571rem;
                height: 1.2857rem;
                line-height: 1.2857rem;
                img{
                    width: auto;
                    height: 1.1429rem;
                    margin-right: 0.2057rem;
                }
                span{
                    margin-top:0.1429rem;
                }
            }
            li:last-child{
                border-right: none;
            }
        }
    }
}
</style>
