<template>
    <div id="body-l">
        <img src='../assets/1.png'/>
        <div class="body1">          
            <span>姓名：刘涛</span>
            <span>学历：专科</span>
            <span>工作年限：1.5年</span>
            <span>年龄：20</span>
            <span>联系电话：19170214694</span>
            <span>电子邮箱：onresize@163.com</span>
            <span>简书：6681</span>
            <span>Github：2069814988</span>
        </div>
    </div>
</template>


<script>
export default {
    
}
</script>


<style scoped>
#body-l{
     margin: 20px;
    width: 320px;
    height: 520px;
    background-color: rgb(24,32,45);
    border-radius: 15px;
    border-top: 4px solid white ;
    border-bottom: 4px solid white ;
}
.body1{
    display: flex;
    flex-direction: column;
    margin-left: 10px;
}
img{
    width: 180px;
    height: 180px;
    border-radius: 50%;
    box-shadow: 0 0 10px #ccc;
    margin-left: 70px;
    margin-top: 10px;
}
span{
    color: white;
    font-size: 22px;
    margin-top:7px;
}
</style>