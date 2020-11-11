<template>
    <div id="home">  
        <Topbar/>  
            <div class="home-a">
                <Bodyl/>
                <Bodyc/>
                <Bodyr/> 
            </div>
            <div class="home-b">
                <footleft/>
                <footcenter/>
                <footright/>            
            </div>           
        <Endbox/>
    </div>
    
</template>

<script>
import Topbar from '../components/topbar'
import Endbox from '../components/endbox'
import Bodyl from '../components/bodyleft'
import Bodyc from '../components/bodycenter'
import Bodyr from '../components/bodyright'
import Footleft from '../components/footleft'
import Footcenter from '../components/footcenter'
import Footright from '../components/footright'

alert('佛曰：\n写字楼里写字间，写字间里程序员\n程序人员写程序，又拿程序换酒钱\n酒醒只在网上坐，酒醉还来网下眠\n酒醉酒醒日复日，网上网下年复年\n但愿老死电脑间，不愿鞠躬老板前\n奔驰宝马贵者趣，公交自行程序员\n别人笑我忒疯癫，我笑自己命太贱\n不见满街漂亮妹，哪个归得程序员\n')

export default {
    data(){
        return{}
    },
    components:{
        Topbar,
        Endbox,
        Bodyl,
        Bodyc,
        Bodyr,
        Footleft,
        Footcenter,
        Footright
    }
}
</script>

<style scoped>
#home{
    height: 100%;
}
.home-a,
.home-b{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}
</style>