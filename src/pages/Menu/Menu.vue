<template>
 <div id="Menu">
    <el-menu id="el_Menu" default-active="/Home" class="el-menu-demo" mode="horizontal" router text-color='#000000' >
        <el-menu-item   index="/Home" ><b>首页</b></el-menu-item>
        <el-menu-item   index="2" disabled><b>技术篇</b></el-menu-item>
        <el-menu-item   index="3" disabled><b>旅行篇</b></el-menu-item>
        <el-menu-item   index="4" disabled><b>随笔</b></el-menu-item>
        <el-menu-item   index="5" disabled><b>关于我</b></el-menu-item>
    </el-menu>
    <!-- <el-menu id="el_Menu" default-active="/Home" class="el-menu-demo" mode="horizontal" router text-color='#000000' >
        <el-menu-item   v-for="item in Menu" :key="item" ><i>{{item.name}}</i></el-menu-item>
    </el-menu> -->
 </div>
</template>
<script>
 export default {
    data () {
      return {
          activeIndex:'1',
           Menu:[
             {
                 name:'首页',
                 path:'/HelloWorld'
             },
              {
                 name:'技术篇',
                 path:'/HelloWorld'
             },
              {
                 name:'旅行篇',
                 path:'/HelloWorld'
             },
              {
                 name:'随笔',
                 path:'/HelloWorld'
             },
              {
                 name:'关于我',
                 path:'/HelloWorld'
             },
         ],


      }
    },
   components: {

   },
   methods:{
       
   }
 }
</script>

<style scoped>
#Menu{
    margin-top: 10px;
    text-align: center;
    width: 100%;
}
#el_Menu{
    margin: 0 auto;
    text-align: center;
}

</style>
