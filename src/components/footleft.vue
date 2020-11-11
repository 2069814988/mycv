<template>
    <div class="footleft" ref="echarts2"></div>
</template>
 
<script>
import echarts from 'echarts'
export default {
 name: 'footleft',
     data () {
         return {
             option: {
    title: {
        text: '爱好分布',
        top: 10,
        left: 10
    },
    tooltip: {
        trigger: 'item',
        backgroundColor: 'rgba(0,0,250,0.2)'
    },
    legend: {
        type: 'scroll',
        bottom: 10,
        data: (function (){
            var list = [];
            for (var i = 1; i <=28; i++) {
                list.push(i + 2000 + '');
            }
            return list;
        })()
    },
    visualMap: {
        top: 'middle',
        right: 10,
        color: ['red', 'yellow'],
        calculable: true
    },
    radar: {
        indicator: [
            { text: '篮球', max: 400},
            { text: '游泳', max: 400},
            { text: '跑步', max: 400},
            { text: '桌球', max: 400},
            { text: 'PUBG', max: 400}
        ]
    },
    series: (function (){
        var series = [];
        for (var i = 1; i <= 28; i++) {
            series.push({
                name: '浏览器（数据纯属虚构）',
                type: 'radar',
                symbol: 'none',
                lineStyle: {
                    width: 1
                },
                emphasis: {
                    areaStyle: {
                        color: 'rgba(0,250,0,0.3)'
                    }
                },
                data: [{
                    value: [
                        (40 - i) * 10,
                        (38 - i) * 4 + 60,
                        i * 5 + 10,
                        i * 9,
                        i * i /2
                    ],
                    name: i + 2000 + ''
                }]
            });
        }
        return series;
    })()
}
         }
     },
     methods:{
          getEcharts(){
            // 基于dom,初始化echarts实例
            let echart = echarts.init(this.$refs.echarts2)
            // 使用刚指定的配置项和数据显示图表
            echart.setOption(this.option);
        }
     },
    mounted(){
         this.getEcharts()
    }
}
</script>
 
<style scoped >
 .footleft{
    margin: 20px;
    width: 650px;
    height: 350px;
    background-color: rgb(24,32,45);
    border-radius: 15px;
    border-top: 4px solid white ;
    border-bottom: 4px solid white ;
 }
</style>