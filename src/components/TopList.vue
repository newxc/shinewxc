<!--
 * @Author: yx
 * @Date: 2019-11-09 10:23:20
 * @LastEditors: yx
 * @LastEditTime: 2019-11-13 09:58:29
 * @Description: 排行榜
 -->

 <template>
  <div class="topList">
      <div class="hello">
          <span class="el-icon-sunny"><i>9°C</i></span>
          <h4 id="welcity">{{cityname}}</h4>
      </div>
      <div class="topCon">
          <p>{{type}}</p>
          <div class="topBox" v-for="(item,index) in tops" :key="index">
              <img :src="item.img">
              <span>热门景点</span>
              <div class="topBoxR">
                  <p>{{item.one1}}</p>
                  <span>票价：￥{{item.price}}起</span>
                  <span>销量：<b>{{item.bycount}}</b></span>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
    name: 'TopList',
    props:['type','cityname'],
    data() {
        return {
            msg:"西安",
            tops:[],
            obj:{
                '最新':'getNews',
                '热销排行榜':'getHot'
            }
        }
    },
    created() {
        console.log(this.cityname);
        fetch('/api/citys')
        .then(res=>{
            return res.json();
        })
        .then(data=>{
            let funcName = this.obj[this.type];
            this.tops = this[funcName](data);
            // this.tops = this[this.obj](data);
        })
        .catch(err=>{
        console.log(err);
        })
    },
    methods: {
        getNews(data){
          let arr = [];
          for(let i in data){
              if(data[i].isNew){
                  arr.push(data[i]);
              }
          }
          return arr;
      },
         getHot(data){
          data.sort(function (obj1,obj2) {
              return obj2.bycount-obj1.bycount;
          });
          let arr = data.slice(0,3);
          return arr;
      }
    },
    mounted() {
		if(this.$route.params.name==null){
            return document.getElementById("welcity").innerHTML='您好，欢迎来到'+'西安';
        }else{
            document.getElementById("welcity").innerHTML='您好，欢迎来到'+this.cityname;
        }

	},
}
</script>

<style scoped>
.topList{
    width: 95%;
    /* overflow: hidden; */
    height: 3.1rem;
    margin: 0 auto;
    /* background: rgb(231, 200, 205); */
    margin-top: 1.5%;
    box-sizing: border-box;
}
.hello{
    width: 95%;
    font-size: 0.18rem;
    line-height: 0.3rem;
}
.hello span{
    float: left;
}
.hello h4{
    margin-left: 30%;
    font-size: 0.16rem;
}
i{
    font-style: normal;
    font-size: 12px;
    vertical-align: top;
}
.topCon{
    width: 93%;
    /* height: 3rem; */
    background: #fff;
    padding: 0.1rem;
    margin-top: 0.08rem;
    border-radius: 0.1rem;
    margin: 0 auto;
    /* box-sizing: border-box; */
    box-shadow: 0rem 0rem 0.05rem 0.01rem #ccc;
}
.topCon>p{
    font-weight: bold;
}
.topBox{
    width: 100%;
    height: 0.7rem;
    background: #f6f6f6;
    margin-top: 0.1rem;
    border-radius: 0.1rem;
     position: relative;
}
.topBox img{
    width: 30%;
    height: 100%;
    float: left;
    border-radius: 0.1rem;
   
}
.topBox>span{
    background: rgb(245, 87, 87);
    position: absolute;
    top: 0;
    left: 0.06rem;
    padding: 0.03rem;
    font-size: 12px;
    color: #fff;
}
.topBoxR{
    float: left;
    margin-left: 0.2rem;
}
.topBoxR p{
    font-size: 0.18rem;
    line-height: 0.4rem;
}
.topBoxR span{
    line-height: 0.3rem;
    margin-right: 0.15rem;
}
</style>
