<!--
 * @Author: yx
 * @Date: 2019-11-08 19:56:05
 * @LastEditors: yx
 * @LastEditTime: 2019-11-13 14:57:34
 * @Description: 详情页
 -->

 <template>
    <div :shopid="this.$route.params.id">
        <Banner></Banner>
        
    </div>
</template>

<script>

import Banner from '../components/Banner';


export default {
  name: 'Des',
  props:[],
  data() {
      return {
          
      }
  },
  components:{
     Banner
  },
  created() {
    //   console.log(this.cityid);
  },
  mounted() {
    console.log("shopid"+this.$route.params.id)
  },
  
}

</script>

<style>
body{
     background: #f6f6f6;
}
</style>
