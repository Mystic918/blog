<!--  -->
<template>
<div class='drawer'>
    <el-drawer
    direction="ltr"
  title="我是标题"
  :visible.sync="drawer"
  :with-header="false"
  :before-close="DrawerOpen"
  >
  
  {{drawer}}
 <el-menu
      default-active="2"
      class="el-menu-vertical-demo">
      <el-menu-item index="2">
        <i class="el-icon-menu"></i>
        <span slot="title">导航二</span>
      </el-menu-item>
      <el-menu-item index="3" disabled>
        <i class="el-icon-document"></i>
        <span slot="title">导航三</span>
      </el-menu-item>
      <el-menu-item index="4">
        <i class="el-icon-setting"></i>
        <span slot="title">导航四</span>
      </el-menu-item>
    </el-menu>

</el-drawer>
</div>
</template>

<script>
import {mapState} from 'vuex'
export default {
components: {},
data() {
    return { 
      };
   },
  computed:mapState(['drawer']),
  methods: {
      DrawerOpen :function(){
         
         this.$store.commit('OPEN_NAV',false)
        
      }
  }
}
</script>
<style lang='scss' scoped>

</style>