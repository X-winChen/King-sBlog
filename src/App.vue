<template>
  <div id="app">
  <Title></Title>
  <Menu></Menu>
  <router-view/> 
  </div>
</template>

<script>
import Title from './pages/Title/Title'
import Menu from './pages/Menu/Menu'
export default {
  name: 'App',
  components:{
    Title:Title,
    Menu:Menu
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
</style>
