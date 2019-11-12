<!--
 * @Author: yx
 * @Date: 2019-11-11 17:42:08
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 20:12:54
 * @Description: 定位
 -->

 <template>
    <div>
      <PosTop></PosTop>
      <City></City>
    </div>
</template>

<script>
import PosTop from '../components/PosTop';
import City from '../components/City';

export default {
  name: 'Positioning',
//   props:['msg'],
  data() {
      return {
          msg:""
      }
  },
  components:{
      PosTop,City
  }
}

</script>

<style>
body{
     background: #f6f6f6;
}
</style>
