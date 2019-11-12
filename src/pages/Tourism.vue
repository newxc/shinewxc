<!--
 * @Author: yx
 * @Date: 2019-11-09 19:48:13
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 19:43:25
 * @Description: 旅游页
 -->

 <template>
    <div>
        <MyTop></MyTop>
        <Banner></Banner>
        <Trip></Trip>
        <TripNav></TripNav>
        <SceneryList></SceneryList>
        <MyFooter></MyFooter>
    </div>
</template>

<script>
import MyTop from '../components/MyTop';
import Banner from '../components/Banner';
import Trip from '../components/Trip';
import TripNav from '../components/TripNav';
import SceneryList from '../components/SceneryList';
import MyFooter from '../components/MyFooter';

export default {
  name: 'Tourism',
  data() {
      return {
          
      }
  },
  components:{
      MyTop,Banner,Trip,TripNav,SceneryList,MyFooter
  }
}

</script>

<style>
body{
     background: #f6f6f6;
}
</style>
