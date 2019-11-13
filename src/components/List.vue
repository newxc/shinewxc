<!--
 * @Author: yx
 * @Date: 2019-11-12 16:57:47
 * @LastEditors: yx
 * @LastEditTime: 2019-11-13 14:40:10
 * @Description: 所有景点
 -->


 <template>
    
    <div class="sceList">
        <h3>所有景点</h3>
        <div class="secL">
             <div class="secBox" v-for="(item,index) in lists" :key="index" @click="lisDes(item.id)">
                <router-link :to='"/Des/"+item.id'>
                    <img :src="item.img">
                    <div class="sceR">
                        <p>{{item.one1}}</p>
                        <span>票价：<i>￥{{item.price}}起</i></span>
                    </div>
                    <div class="jd">景点</div>
                </router-link>
            </div>
        </div>
        <div class="secL">
             <div class="secBox" v-for="(item,index) in lists" :key="index">
                <img :src="item.img">
                <div class="sceR">
                    <p>{{item.one1}}</p>
                    <span>票价：<i>￥{{item.price}}起</i></span>
                </div>
                 <div class="jd">景点</div>
            </div>
        </div>
        <div class="secL">
             <div class="secBox" v-for="(item,index) in lists" :key="index">
                <img :src="item.img">
                <div class="sceR">
                    <p>{{item.one1}}</p>
                    <span>票价：<i>￥{{item.price}}起</i></span>
                </div>
                 <div class="jd">景点</div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'List',
  props:['type'],
  data() {
      return {
            lists:[],
            shopDesid:''
      }
  },
  created() {
      axios.get('/api/citys')
      .then(res=>{
          let newshop = [];
        //   this.lists = res.data;
          for(let i in res.data){
              if(res.data[i].price){
                  newshop.push(res.data[i])
              }
              else{
                  continue;
              }
          }
        //   return newshop;
          this.lists = newshop;
          console.log( this.scenerys)
        //   console.log(res.data);
      })
      .catch(err=>{
          console.log(err);
      })
  },
    methods: {
        lisDes(id){
            // console.log(id);
            this.shopDesid = id;
            console.log(this.shopDesid);
        }
    },
}

</script>

<style scoped>
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
.secL a{
    color: black;
}
.secBox{
    width: 45%;
    /* height: 1.7rem; */
    padding-bottom: 0.08rem;
    position: relative;
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
.jd{
    width: 0.35rem;
    height: 0.2rem;
    background: rgb(0,0,0,0.7);
    color: #ddd;
    font-size: 0.12rem;
    line-height: 0.2rem;
    text-align: center;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 15;
    border-top-left-radius: 0.08rem;
    border-bottom-right-radius: 0.04rem;
}
</style>
