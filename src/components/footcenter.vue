<template>
 <div class="footcenter">
     <div class="footcenter-a">
        <h3>编程技能</h3>
        <div style="color:skyblue"><strong>前端：</strong></div>
        <div style="color:white">HTML/H5,CSS/CSS3、JS/ES6、jQuery、Vue、React、小程序</div>
        
        <div style="color:skyblue"><strong>开发环境：</strong></div>
        <div style="color:white">Node、phpstudy、VsCode、Hubilderx</div>

        <div style="color:skyblue"><strong>数据库：</strong></div>
        <div style="color:white">MongoDB、Mysql</div>

        <div style="color:skyblue"><strong>其他：</strong></div>
        <div style="color:white">Git、Svn</div>
    </div>
 </div>
</template>

 
<script>
export default {
 name: 'footcenter',
     data () {
         return {}
     },
     methods:{},
     components:{}
}
</script>
 
<style scoped >
 .footcenter{
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
.footcenter-a{
    width: 280px;
    height: 300px;
    /* background-color:pink; */
    padding-left: 19px;
}
</style>