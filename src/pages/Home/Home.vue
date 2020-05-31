<template>
 <div id="Home">
    <div id="carousel">
        <el-carousel  type="card" class="el-carousel__container">
            <el-carousel-item v-for="(item,index) in imgs" :key="index" >
                <el-image :src="item.url" fit="none" />
            </el-carousel-item>
        </el-carousel>
    </div>
    <el-divider  content-position="left"><span class="divider"> if(1=1) </span></el-divider>
    <div class="block">
  <el-timeline>
    <el-timeline-item timestamp="2018/4/12" placement="top">
      <el-card>
        <el-link type="info" @click="toUrl('/HelloWorld')">Unity3D -- 环境搭建</el-link> <br/>
        <el-tag>Unity3D</el-tag>
        <el-drawer
          title="我是标题"
          :visible.sync="drawer"
          :with-header="false"
          size='70%'>
          <Article></Article>
        </el-drawer>
      </el-card>
    </el-timeline-item>
    <el-timeline-item timestamp="2018/4/3" placement="top">
      <el-card>
        <el-link type="info" @click="toUrl('/HelloWorld')">Vue -- 搭建Vue-ci</el-link> <br/>
        <el-tag type="success">Vue</el-tag>
      </el-card>
    </el-timeline-item>
    <!-- <el-timeline-item timestamp="2018/4/2" placement="top">
      <el-card>
        <el-link type="info">更新 Github 模板</el-link> 
      </el-card>
    </el-timeline-item> -->
  </el-timeline>
</div>
    <el-divider  content-position="left"><span class="divider"> Print " Hello World! " </span></el-divider>
    <el-divider  content-position="left"><span class="divider"> Print " Hello World! " </span></el-divider>
 </div>
</template>

<script>
import Article from '../Article/Article'
 export default {
   data () {
     return {
         imgs:[
             {
                 url:require('../../../Img/1.jpg'),
             },
              {
                 url:require('../../../Img/2.jpg'),
             },
             {
                 url:require('../../../Img/4.jpg'),
             },
             {
                 url:require('../../../Img/5.jpeg'),
             }           
         ],//图片资源列表
         drawer:false
     }
   },
   components: {
     Article:Article

   },
   methods:{
       toUrl(path){
           //this.$router.push({path:path});
           this.drawer=true;
       }
   }
 }
</script>

<style>
.imgs{
    width: auto;
}
#Home{
    margin-top: 20px;
}
.divider{
    color: #909399;
    font-family: "Helvetica Neue" ;
}
#carousel{
    height: 400px;
}
@media(max-width:76.375rem){
	#carousel{
		height: 200px ;
    }
}
.el-carousel__container{
    width: 100%;
    height: 90%!important;
}

</style>
