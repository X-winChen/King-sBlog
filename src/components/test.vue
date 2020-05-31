<template>
  <div id="test">
    <p>测试</p>
    <router-link  to="/HelloWorld">Home</router-link>
    <router-view />
    <router-link  to="/test">Home</router-link>
  </div>
</template>

<script>
import { Toast } from "vant";
import { Dialog } from "vant";
export default {
  name: 'test',
  data(){
    return{
      isshow:true
    }
  }
}
</script>

<style>

</style>
