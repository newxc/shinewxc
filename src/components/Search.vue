<!--
 * @Author: yx
 * @Date: 2019-11-08 20:00:17
 * @LastEditors: yx
 * @LastEditTime: 2019-11-13 14:36:13
 * @Description: 搜索栏
 -->

 <template>
  <div class="box" >
    <router-link to="/Positioning"><span id="city">{{cityname}} </span><span class="el-icon-arrow-down"></span></router-link>
    <input type="text" placeholder="陕西历史博物馆门票">
	<span class="el-icon-microphone"></span>
    <router-link to="/CustService"><span class="el-icon-chat-dot-round"></span></router-link>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'Search',
  props:['id','cityname'],
  data() {
      return {
		  msg:"西安",
		  city:{},
		  citys:[],
		//   cityid:[]
      }
  },
//   created() {
	
// 	   axios.get('http://localhost:3000/citys'+this.id)
//       .then(res=>{

// 		  	console.log(res.data);
//          	this.book = res.data;
			
//       })
//       .catch(err=>{
//           	console.log(err);
//       })
//   },
  mounted() {
	//   console.log(cityname);
		if(this.$route.params.name==null){
            return document.getElementById("city").innerHTML='西安';
        }else{
            document.getElementById("city").innerHTML=this.cityname;
        }

	},
  
	methods: {
	}
}
</script>

<style scoped>
.box{
    width: 100%;
	height: 0.24rem;
	margin: 0 auto;
	font-size: 0.16rem;
	position: fixed;
	left: 0;
    top: 0;
	z-index: 20;
	background-color: rgba(255,255,255,0.8);
	padding: 0.1rem;
	
}
.box a{
	float: left;
	/* font-size: 0.14rem; */
	width: 0.5rem;
}
.box a span{
	font-size: 0.14rem;
	
}
.box span{
    float: left;
	color: black;
	/* color: #fff; */

}
.box .el-icon-microphone{
	color: black;
}
.el-icon-arrow-down{
	margin-top: 0.03rem;
	margin-right: 0.02rem;
}
.box :nth-child(3){
	font-size: 0.18rem;
	position: absolute;
	right: 18%;
	top: 30%;
}
.box input{
    width: 70%;
	height: 100%;
	/* background: #eee; */
	background-color: #fff;
	border-radius: 0.19rem;
	float: left;
	border: 0;
	text-indent: 0.28rem;
	margin-left: 0.07rem;
	background-image: url(../assets/img/home-common-sprite2x@v7.15.png);
	background-repeat: no-repeat;
	background-position: 8px 5px;
	background-size: 0.20rem;
	outline: none;
}
.box :last-child span{
	float: left;
	margin-left: 0.1rem;
	font-size: 0.18rem;
}
</style>
