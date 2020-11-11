<template>
    <div class="bodyr">
        <div id="body-r">
            <div class="top-r">{{abc}}</div> 
            <div class="bodyright-a" ref="echarts1"></div>  
        </div>   
    </div>  
</template>


<script>
import moment from 'moment'
import echarts from 'echarts'
export default {
    data(){
        return{
            abc:'',
            option: {
    title: {
        text: '踩坑形势图分布',
        left: 'center'
    },
    xAxis: {
        type: 'category',
        boundaryGap: false
    },
    yAxis: {
        type: 'value',
        boundaryGap: [0, '30%']
    },
    visualMap: {
        type: 'piecewise',
        show: false,
        dimension: 0,
        seriesIndex: 0,
        pieces: [{
            gt: 1,
            lt: 3,
            color: 'rgba(0, 180, 0, 0.5)'
        }, {
            gt: 5,
            lt: 7,
            color: 'rgba(0, 180, 0, 0.5)'
        }]
    },
    series: [
        {
            type: 'line',
            smooth: 0.6,
            symbol: 'none',
            lineStyle: {
                color: 'green',
                width: 5
            },
            markLine: {
                symbol: ['none', 'none'],
                label: {show: false},
                data: [
                    {xAxis: 1},
                    {xAxis: 3},
                    {xAxis: 5},
                    {xAxis: 7}
                ]
            },
            areaStyle: {},
            data: [
                ['2020-3月', 100],
                ['2020-4月', 200],
                ['2020-5月', 400],
                ['2020-6月', 650],
                ['2020-7月', 500],
                ['2020-8月', 250],
                ['2020-9月', 300],
                ['2020-10月', 750],
                ['2020-11月', 300]
               
            ]
        }
    ]
}
        }
    },
    methods:{
        getEcharts(){
            // 基于dom,初始化echarts实例
            let echart = echarts.init(this.$refs.echarts1)
            // 使用刚指定的配置项和数据显示图表
            echart.setOption(this.option);
        }
    },
    created(){
      setInterval(() => {
          this.abc = moment().format('HH:mm:ss');
        },1000)
    },
    mounted(){
         this. getEcharts()
    }
}
</script>


<style scoped>
#body-r{
     margin: 20px;
    /* margin-left: 40px; */
    width: 400px;
    height: 520px;
    background-color: rgb(24,32,45);
    border-radius: 15px;
    border-top: 4px solid white ;
    border-bottom: 4px solid white ;
}
.top-r{
        height: 55px;
        width: 399px;
        border-radius: 10px;
        font-size: 35px;
        background-color:rgb(24,32,45);
        font-weight: bold;
        font-family:'楷体';
        display: inline-block;
        line-height: 55px;
        text-align: center;
        color: pink;
    }
    .bodyright-a{
        height: 450px;
        width: 399px;
    }
</style>