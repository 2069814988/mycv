<template>
    <div id="topbar"> 
                 
    </div>
    <!-- 每天坚持踩坑(仍未猝死) -->
       
</template>

<script>

export default{
    name:'topbar',
    data(){
        return{

        }
    }
}

    console.log([
      "                   _ooOoo_",
      "                  o8888888o",
      "                  88\" . \"88",
      "                  (| -_- |)",
      "                  O\\  =  /O",
      "               ____/`---'\\____",
      "             .'  \\\\|     |//  `.",
      "            /  \\\\|||  :  |||//  \\",
      "           /  _||||| -:- |||||-  \\",
      "           |   | \\\\\\  -  /// |   |",
      "           | \\_|  ''\\---/''  |   |",
      "           \\  .-\\__  `-`  ___/-. /",
      "         ___`. .'  /--.--\\  `. . __",
      "      .\"\" '<  `.___\\_<|>_/___.'  >'\"\".",
      "     | | :  `- \\`.;`\\ _ /`;.`/ - ` : | |",
      "     \\  \\ `-.   \\_ __\\ /__ _/   .-` /  /",
      "======`-.____`-.___\\_____/___.-`____.-'======",
      "                   `=---='",
      "^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^",
      "         佛祖保佑       永无BUG",
      "---------------------------------------------",
      "           小破站采用Vue响应式框架搭建",
      "           包含插件有moment,Echarts",
    ].join('\n'));

</script>


<style scoped>
    #topbar{
        width: 100%;
        height: 65px;
        background-color: rgb(24,32,45);
        border-bottom: 4px solid white;
        /* position: relative; */
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .top-l{
        height: 55px;
        width: 300px;
        background-color: white;
        border-radius: 50px;
        margin: 5px;
    }
</style>