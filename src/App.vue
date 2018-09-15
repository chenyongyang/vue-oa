<template>
  <div id="app">
    <Header></Header>
    <Menu></Menu>
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/Header'
import Menu from '@/components/Menu'
export default {
  components:{
    Header,Menu
  }
}
</script>

<style>
*{
  list-style: none;
  margin: 0;
  padding: 0;
  text-decoration: none;
}
#app{
  background: #eee
}
</style>
