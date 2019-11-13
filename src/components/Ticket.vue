<!--
 * @Author: yx
 * @Date: 2019-11-08 22:31:20
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 14:43:15
 * @Description: 
 -->

 <template>
  <div>
       <table class="ticket">
        <tr>
            <td><a href="#">酒店</a></td>
            <td><a href="#">民宿</a></td>
            <td colspan="2"><a href="#">机票/火车票+酒店</a></td>
        </tr>
        <tr>
            <td><a href="#">机票</a></td>
            <td><a href="#">火车票</a></td>
            <td><a href="#">汽车·船票</a></td>
            <td><a href="#">打车·租车</a></td>
        </tr>
        <tr>
            <td><router-link to="/Tourism">旅游</router-link></td>
            <td><a href="#">高铁游</a></td>
            <td><a href="#">邮轮游</a></td>
            <td><a href="#">定制游</a></td>
        </tr>
    </table>
     <div class="serviceNav">
        <a href="#">
            <span></span>
            <p>自由行</p>
        </a>
        <a href="#">
            <span></span>
            <p>WiFi电话卡</p>
        </a>
        <a href="#">
            <span></span>
            <p>保险·签证</p>
        </a>
        <a href="#">
            <span></span>
            <p>换外币·购</p>
        </a>
        <a href="#">
            <span></span>
            <p>当地向导</p>
        </a>
        <a href="#">
            <span></span>
            <p>特价机票</p>
        </a>
        <a href="#">
            <span></span>
            <p>礼品卡</p>
        </a>
        <a href="#">
            <span></span>
            <p>申卡·借钱</p>
        </a>
        <a href="#">
            <span></span>
            <p>旅拍</p>
        </a>
        <a href="#">
            <span></span>
            <p>更多</p>
        </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Ticket',
  data() {
      return {
         
      }
  }
}
</script>

<style scoped>
.ticket{
	width: 95%;
	/* height: 1.7rem; */
	font-size: 14px;
	text-align: center;
	border-collapse: collapse;
	margin: 0 auto;
    /* margin-top: -5%; */
    margin-top: 2.5%;
}
.ticket tr:nth-child(1){
    background:#fb7c52;
} 
.ticket tr:nth-child(2){
    background:#51b4ed;
} 
.ticket tr:nth-child(3){
    background:#4cca88;
} 
.ticket tr:first-child td:first-child{
    border-top-left-radius:0.1rem;
    background: url(../assets/img/1.png) no-repeat right bottom;
    background-size: 80% 60%;
}
.ticket tr:first-child td:last-child{
    border-top-right-radius:0.1rem;
    background: url(../assets/img/3.png) #ffc04b no-repeat right bottom;
    background-size: 80% 60%;
}
.ticket tr:nth-child(2) td:first-child{
    background: url(../assets/img/4.png) no-repeat right bottom;
    background-size: 80% 60%;
}
.ticket tr:last-child td:first-child{
    border-bottom-left-radius:0.1rem;
    background: url(../assets/img/8.png) no-repeat right bottom;
    background-size: 80% 60%;
}
.ticket tr:last-child td:last-child{
    border-bottom-right-radius:0.1rem;
}
.ticket td{
	width: 0.68rem;
	height: 0.5rem;
	border: 1px solid #f6f6f6;
}
.ticket td a{
    color: #fff;
}
.ticket tr td:first-child{
	width: 33%;
	text-align: left;
	text-indent: 0.2rem;
}
.serviceNav{
	width: 95%;
	height: 1rem;
	/* background: #fff; */
	margin: 0 auto;
	display: flex;
	justify-content: space-around;
    flex-wrap: wrap;
    margin-top: 0.1rem;
}
.serviceNav a{
    display: block;
    width: 20%;
    height: 0.35rem;
    text-align: center;
    color: black;
}
.serviceNav a span{
    display: block;
    width: 0.25rem;
	height: 0.25rem;
    overflow: hidden;
    margin: 0 auto;
    background-image: url(../assets/img/un_ico_subnav2x@v7.152.png);
	background-repeat: no-repeat;
	background-size: 0.25rem;
}
.serviceNav a:nth-child(1) span{
	background-position:  0px 0px;
}
.serviceNav a:nth-child(2) span{
	background-position:  0px -0.25rem;
}
.serviceNav a:nth-child(3) span{
	background-position:  0px -0.5rem;
}
.serviceNav a:nth-child(4) span{
	background-position:  0px -0.75rem;
}
.serviceNav a:nth-child(5) span{
	background-position:  0px -1rem;
}
.serviceNav a:nth-child(6) span{
	background-position:  0px -1.25px;
}
.serviceNav a:nth-child(7) span{
	background-position:  0px -1.5rem;
}
.serviceNav a:nth-child(8) span{
	background-position:  0px -1.75rem;
}
.serviceNav a:nth-child(9) span{
	background-position:  0px -2rem;
}
.serviceNav a:nth-child(10) span{
	background-position:  0px -2.25rem;
}
.serviceNav p{
    font-size: 12px;
}
</style>
