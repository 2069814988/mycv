<template>
    <div id="body-c" ref="echarts"></div>
</template>


<script>
import echarts from 'echarts'
export default {
    data(){
        return{
            option:{
    title: {
        text: '技能分布图',
        left: 'center'
    },
    tooltip: {
        trigger: 'item',
        formatter: '{a} <br/>{b} : {c} ({d}%)'
    },
    legend: {
        left: 'center',
        top: 'bottom',
        data: ['html', 'css', 'javascript', 'jquery', 'Vue', 'php', 'node', '小程序']
    },
    toolbox: {
        show: true,
        feature: {
            mark: {show: true},
            dataView: {show: false, readOnly: false},
            magicType: {
                show: true,
                type: ['pie', 'funnel']
            },
            restore: {show: false},
            saveAsImage: {show: false}
        }
    },
    series: [
        {
            name: '半径模式',
            type: 'pie',
            radius: [20, 110],
            center: ['25%', '50%'],
            roseType: 'radius',
            label: {
                show: false
            },
            emphasis: {
                label: {
                    show: true
                }
            },
            data: [
                {value: 40, name: 'html'},
                {value: 35, name:  'css'},
                {value: 15, name: 'javascript'},
                {value: 20, name: 'jquery'},
                {value: 30, name: 'Vue'},
                {value: 25, name: 'php'},
                {value: 5, name: 'node'},
                {value: 10, name: '小程序'}
            ]
        },
        {
            name: '面积模式',
            type: 'pie',
            radius: [30, 110],
            center: ['75%', '50%'],
            roseType: 'area',
            data: [
                {value: 40, name: 'html'},
                {value: 35, name: 'css'},
                {value: 15, name: 'javascript'},
                {value: 20, name: 'jquery'},
                {value: 30, name: 'Vue'},
                {value: 25, name: 'php'},
                {value: 5, name: 'node'},
                {value: 10, name: '小程序'}
            ]
        }
    ]
}

        }
    },
    methods:{
        getEcharts(){
            // 基于dom,初始化echarts实例
            let echart = echarts.init(this.$refs.echarts)
            // 使用刚指定的配置项和数据显示图表
            echart.setOption(this.option);
        }
    },
    mounted(){
         this.getEcharts()
    }
}
</script>


<style scoped>
#body-c{
    margin: 20px;
    /* margin-left: 40px; */
    width: 600px;
    height: 528px;
    background-color: white;
    border-radius: 15px;
    border-left: 4px solid rgb(24,32,45);
    border-right: 4px solid rgb(24,32,45) ;
}

</style>