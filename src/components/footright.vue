<template>
 <div class="footright">
     <div class="footright-a">
         <h3>求职意向</h3>
        <div style="color:skyblue">期望职位：<span style="color:white">前端工程师</span></div>       
        <div style="color:skyblue">理想大厂：<span style="color:white">Byte Dance</span></div>       
        <div style="color:skyblue">工作技能：<span style="color:white">Vue</span></div>      
        <div style="color:skyblue">目标城市：<span style="color:white">杭州、广州、上海、厦门</span></div>  
        <div style="color:skyblue">希望薪资：<span style="color:white">5k-8k</span></div>    
     </div>
 </div>
</template>
 
<script>
export default {
 name: 'footright',
     data () {
         return {}
     },
     methods:{},
     components:{}
}
</script>
 
<style scoped >
 .footright{
    margin: 20px;
    width: 300px;
    height: 350px;
    background-color: rgb(24,32,45);
    border-radius: 15px;
    border-top: 4px solid white ;
    border-bottom: 4px solid white ;
 }
  h3{
     color: white;
     text-align: center;
 }
 .footright-a{
    width: 280px;
    height: 300px;
    /* background-color:pink; */
    padding-left: 19px;
}
.footright-a div{
    margin-top: 12px;
}
</style>