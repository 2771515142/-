<template>
  <div class="test-container">
    <ImageLoader 
      src="https://images.pexels.com/photos/33109/fall-autumn-red-season.jpg?fit=crop&crop=entropy&w=3456&h=2304"
      placeholder="https://images.pexels.com/photos/33109/fall-autumn-red-season.jpg?w=100"
      :duration="1000"
      @load = "handleLoaded"
    />
  </div>
  
</template>

<script>
import ImageLoader from "./";
export default {
    components:{
       ImageLoader 
    },
    methods:{
      handleLoaded(){
        console.log("ImageLoader组件load事件触发，图片加载完毕");
      }
    }
}
</script>

<style>
  .test-container{
    width:500px;
    height:400px;
    border:solid 2px;
    margin:0 auto;
  }
</style>