<!--
 * @Author: yx
 * @Date: 2019-11-11 20:11:05
 * @LastEditors: yx
 * @LastEditTime: 2019-11-12 10:40:30
 * @Description: 城市
 -->

<template>
    <div class="city">
       <div class="now">
           <p>当前/历史</p>
           <ul>
               <li><span class="el-icon-location"></span> 西安</li>
               <li>渭南</li>
               <li>北京</li>
           </ul>
       </div>
       <div class="hot">
            <p>热门城市</p>
           <ul>
               <li v-for="(item,index) in citys" :key="index"><router-link :to='"/Index/"+item.name'>{{item.name}}</router-link></li>
           </ul>
       </div>
       <div class="quarter">
           <p>当季必玩</p>
           <ul>
               <li  v-for="(item,index) in quarterCity" :key="index">
                    <router-link :to='"/Index/"+item.name'>
                        <img :src="item.img1">
                        <span>{{item.name}}</span>
                    </router-link>
               </li>
           </ul>
       </div>
    </div>  
</template>

<script>
import axios from 'axios';
export default {
  name: 'City',
//   props:['id','cityname'],
  data () {
    return {
      citys:[],
      quarterCity:[],
    //   cityid:[]
    }
  },
  created() {
      axios.get('http://localhost:3000/citys')
      .then(res=>{
        //   console.log(this.id)
          this.citys = res.data;
          for(let i in res.data){
            //   let idarr = [];
            //   this.cityid.push(res.data[i].id);
            //   console.log(res.data[i].id);
          }
        //   console.log(this.cityid);
          let arr = [];
          arr = res.data.slice(0,6);
          this.quarterCity = arr;
          
      })
      .catch(err=>{
          console.log(err);
      })
  },
  methods: {
      
  },
}
</script>

<style scoped>

.city{
    width: 100%;
    margin-top: 0.7rem;
    padding: 0 0.15rem;
    box-sizing: border-box;
}
.city p{
    line-height: 0.3rem;
    font-size: 0.14rem;
}
.city li{
    font-size: 0.14rem;
}
.city a{
    color: black;
}
.now{
    width: 100%;
    overflow: hidden;
    /* margin-bottom: 0.13rem; */
}
.city ul{
    width: 100%;
    overflow: hidden;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
.city ul li{
    width: 31%;
    height: 0.28rem;
    background: rgba(228, 226, 226, 0.842);
    border-radius: 0.03rem;
    line-height: 0.28rem;
    text-align: center;
    margin-bottom: 0.13rem;
}
.now span{
    color: rgb(26, 93, 238);
    font-size: 0.16rem;
}

.hot ul{
    width: 100%;
    overflow: hidden;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
.quarter{
    width: 100%;
    overflow: hidden;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
.quarter ul li{
    height: 0.9rem;
    background: #f6f6f6;
}
.quarter ul{
    width: 100%;
    overflow: hidden;
}
.quarter img{
    width: 100%;
    height: 0.6rem;
    border-radius: 0.04rem;
}
.quarter span{
    line-height: 0.2rem;
}
</style>
