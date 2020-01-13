<template>
  <div class="home">
   <el-row class="container">
     <el-col :xs="24" :sm="24" :md="16" :lg="12" :xl="12" class="swiper-wrap">
        <el-carousel :interval="5000" arrow="always" class="swiper">
          <el-carousel-item v-for="item in 4" :key="item">
            <h3>{{ item }}</h3>
          </el-carousel-item>
        </el-carousel>
     </el-col>
     <el-col :xs="24" :sm="24" :md="8" :lg="12" :xl="12" class="hidden-sm-and-down">
       <el-row>
          <el-col :span="12"><div>1</div><div>2</div></el-col>
          <el-col :span="12"><div>123</div></el-col>
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
   @media screen  and (max-width: 1200px){
     .home{
       width: 98%;
       margin: 0px auto;
     }
   }
 .home{
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
   }
 }
</style>
