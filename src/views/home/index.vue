<template>
  <div class="home">
   <el-row class="container">
     <el-col :xs="24" :sm="16" :md="16" :lg="12" :xl="12" class="swiper-wrap">
     <!-- 轮播图 -->
        <el-carousel :interval="5000" arrow="always" class="swiper">
          <el-carousel-item v-for="item in 4" :key="item">
            <h3>{{ item }}</h3>
          </el-carousel-item>
        </el-carousel>
     </el-col>
     <el-col :xs="24" :sm="8" :md="8" :lg="12" :xl="12" class="hidden-xs-only card">
       <el-row class="hidden-sm-and-dowm">
          <el-col :xs="24" :sm="24" :md="24" :lg="12" :xl="12" >
            <el-row class="view-wrap">
              <el-col  :span="24" class="cardImg"><img src="./images/h1.jpg"></el-col>
              <el-col  :span="24" class="cardImg"><img src="./images/h1.jpg"></el-col>
            </el-row>
          </el-col>
          <el-col  :xs="24" :sm="24" :md="24" :lg="12" :xl="12"  class="hidden-md-and-down personality-wrap">
                <!-- 人物信息 -->
                <div class="personality">
                  <div class="title">DeveloperNote</div>
                  <div class="content">
                    <p>职业：Web前端</p>
                    <p>现居：广东-广州</p>
                    <p>Email：2437300148@qq.com</p>
                    <p>座右铭：90后加班狂人，梦想想成为一名大侠，行侠仗义，浪迹天涯</p>
                  </div>
                  <div class="icon-wrap">
                    <span class="iconfont icon-person person"></span>
                    <span class="iconfont icon-qq qq"></span>
                    <span class="iconfont icon-wechat wechat"></span>
                    <span class="iconfont icon-email email"></span>
                  </div>
                </div>
          </el-col>
      </el-row>
     </el-col>
   </el-row>
  </div>
</template>

<script>

export default {
  name: 'home',
  components: {
  }
}
</script>
<style lang="scss" scoped>

 .home{
        width: 1200px;
       margin: 0px auto;
   .container{
     margin-top: 20px;
      .swiper-wrap{
        .swiper{
          border-radius: 10px;
        }
      }
      .el-carousel__item h3 {
        color: #475669;
        font-size: 18px;
        opacity: 0.75;
        line-height: 300px;
        margin: 0;
      }
      
      .el-carousel__item:nth-child(2n) {
        background-color: #99a9bf;
      }
      
      .el-carousel__item:nth-child(2n+1) {
        background-color: #d3dce6;
      }

         .card{ padding:0px 10px;
           .view-wrap{
             .cardImg{
               display: flex;
               justify-content:center;
               overflow: hidden;
               border-radius: 10px;
               &.cardImg:first-child{margin-bottom: 10px;}
             img{
               border-radius: 10px;
               width: 100%;
               height: 144px;
               margin: 0px auto;
               text-align: center;
             }
             }
           }
          .personality-wrap{
              padding: 0px 10px;
            .personality{
              padding: 20px 10px;
              background-color:rgba(42,42,42,1);
              height: 260px;
              border-radius: 10px;
              .title{ 
                line-height: 50px;
                color: #89919a;
                font-size: 22px;
              }
              .content{
                p{
                color: #d0d2d4;
                font-size: 12px;
                line-height: 28px;
                }
              }
              .icon-wrap{ 
                margin-top: 20px;
                display: flex;
                justify-content:space-between;
                .iconfont{
                  font-size: 28px;
                  display: flex;
                  justify-content: center;
                  align-items: center;
                  width: 50px;
                  height: 50px;
                  border-radius: 25px;
                  background-color: #2a2a2a;
                  box-shadow:1px 1px 1px 1px #000 inset,-1px -1px 1px 1px #000 ;
                }
                .person{color: #ef5509;}
                .qq{color: #1296DB;}
                .wechat{color: #07AF12;}
                .email{color: #FF991A;}
              }


            }

           }
         }
   }
 }
    @media screen  and (max-width: 1200px){
     .home{
       width: 98%;
       margin: 0px auto;
       .container{
         .card{
           .view-wrap{
             .cardImg{
               display: flex;
               justify-content:center;
               overflow: hidden;
             img{
              width: 100%;
               height: 144px;
               margin: 0px auto;
               text-align: center;
             }
             }
           }
           
         }
       }
     }
   }
</style>
