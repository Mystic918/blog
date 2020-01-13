<template>
  <div id="app">
    <Drawer/>
    <Header @DrawerOpen="DrawerOpen"></Header>
      <div class="main">
        <router-view/>
      </div>
    
  </div>
</template>
<script>
import Header from '@/components/Header'
import Drawer from '@/components/drawer'
export default {
  components: {
    Header,
    Drawer
  },
  methods: {
    DrawerOpen:function(){
      
    }
  }
  
}
</script>
<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  .main{
    width: 1200px;
    margin: 0px auto;
  }
  @media screen and (max-width: 1220px) {
    
  .main{
    width: 100%; 
    }
  }
}
</style>
