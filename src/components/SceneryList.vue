<!--
 * @Author: yx
 * @Date: 2019-11-08 23:35:12
 * @LastEditors: yx
 * @LastEditTime: 2019-11-12 14:20:45
 * @Description: 风景列表
 -->

 <template>
    
    <div class="sceList">
        <h3>热门景点</h3>
        <div class="secL">
             <div class="secBox" v-for="(item,index) in scenerys" :key="index">
                <img :src="item.img">
                <div class="sceR">
                    <p>{{item.name}}</p>
                    <span>票价：<i>￥{{item.price}}起</i></span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'SceneryList',
  props:['type'],
  data() {
      return {
          scenerys:[],
          obj:{
                '最新':'getNews',
            }
      }
  },
  created() {
      axios.get('http://localhost:3000/citys')
      .then(res=>{
          let newshop = [];
          this.scenerys = res.data;
          for(let i in res.data){
              if(res.data[i].isNew){
                  newshop.push(res.data[i])
              }
              else{
                  continue;
              }
          }
        //   return newshop;
          this.scenerys = newshop;
          console.log( this.scenerys)
        //   console.log(res.data);
      })
      .catch(err=>{
          console.log(err);
      })
  },
 
}

</script>

<style>
.sceList{
    width: 95%;
    overflow: hidden;
    margin: 0 auto;
    margin-top: 2.5%;
    margin-bottom: 0.5rem;
}
.sceList h3{
    width: 100%;
    height: 0.3rem;
    /* text-align: center; */
    margin-left: 0.1rem;
    font-size: 14px;
    font-weight: bold;
}
.secL{
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
}
.secBox{
    width: 47.5%;
    /* height: 1.7rem; */
    padding-bottom: 0.08rem;
}
.secBox img{
    width: 100%;
    height: 1.5rem;
    border-top-left-radius: 0.08rem;
    border-top-right-radius: 0.08rem;
}
.sceR{
    padding: 0.05rem;
    background: #fff;
}
.sceR p{
    line-height: 0.24rem;
}
.sceR span{
    font-size: 12px;
}
.sceR i{
    color: rgb(250, 68, 68);
    font-size: 14px;
}
</style>
