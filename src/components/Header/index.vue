<template>
<div class='header'>
   <el-row class="nav-wrap">
      <el-col :xs="2" :sm="2" :md="1" class="hidden-md-and-up drawer" ><div class="el-icon-s-unfold" @click="DrawerOpen"></div></el-col>
      <el-col :xs="20" :sm="20" :md="4" :lg="3" :xl="1" class="title">个人博客&nbsp;|&nbsp;技术栈</el-col>
      <el-col :xs="20" :sm="20" :md="19" :lg="19" :xl="22"  class="hidden-sm-and-down">
         <el-menu :default-active="activeIndex" 
         background-color='transparent' 
         active-text-color='#00c1de' 
         mode="horizontal" 
         text-color="#fff"
         class="nav"
         >
               <el-menu-item index="1"><a target="_blank">网站首页</a></el-menu-item>
               <el-menu-item index="2"><a target="_blank">博客专题</a></el-menu-item>
               <el-menu-item index="3" disabled>时间轴</el-menu-item>
               <el-menu-item index="4"><a target="_blank">关于我</a></el-menu-item>
               <el-menu-item index="5"><a target="_blank">留言</a></el-menu-item>
            </el-menu>
      </el-col>
      <el-col :xs="2" :sm="2" :md="1" :lg="1" :xl="1"><div class="el-icon-search search-button"></div></el-col>
</el-row>
</div>
</template>
<script>
import 'element-ui/lib/theme-chalk/display.css';
export default {
components: {},
data() {
    return {
       activeIndex:"1"
      };
   },
   methods: {
      DrawerOpen :function(){
         
         this.$store.commit('OPEN_NAV',true)
        
      }
   }
}
</script>
<style lang='scss' scoped>
.header{
       margin-top: 5px;
   height: 60px;
   background-color: #1c2327;
   line-height: 65px;
   color: #fff;
    &.header::before {
    background: #000 linear-gradient(to left, #4cd964, #5ac8fa, #007aff, #34aadc, #5856d6, #ff2d55);
    content: "";
    height: 5px;
    position: absolute;
    top: 0;
    width: 100%;
   }
   .nav-wrap{
      width: 1200px;
      margin: 0px auto;
      >.el-col{
             height: 60px;
      }
      .search-button{
         font-size: 40px;
         display: flex;
         height: 60px;
         flex-direction:row;
         align-items: center;
         justify-content: center;
         cursor: pointer;
         }
      .drawer{
         font-size: 40px;
         display: flex;
         height: 60px;
         flex-direction:row-reverse;
         align-items: center;
         cursor: pointer;
      }
      .title{
         text-align: center;
         font-size: 22px;
      }
      .nav{
         display: flex;
         justify-content: center;
         .el-menu-item:hover{
               background-color: #000 !important;
               
         }
      }
   }
}
@media screen  and (max-width: 1200px){
   .header{
      .nav-wrap {
         width: 100%;
         .nav{
            li{
               padding: 0 10px;
            }
         }

   }
}

      }
      </style>    