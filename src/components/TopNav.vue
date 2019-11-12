<!--
 * @Author: yx
 * @Date: 2019-11-08 22:18:39
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 09:50:54
 * @Description: 顶部导航
 -->

 <template>
	  <div class="topNav">
        <a href="#">
            <span></span>
            <p>景点·攻略</p>
        </a>
        <a href="#">
            <span></span>
            <p>门票·玩乐</p>
        </a>
        <a href="#">
            <span></span>
            <p>美食林</p>
        </a>
        <a href="#">
            <span></span>
            <p>周边游</p>
        </a>
        <a href="#">
            <span></span>
            <p>一日游</p>
        </a>
    </div>
</template>

<script>
export default {
  name: 'TopNav',
  data() {
      return {
          
	  }
  }
}
</script>

<style>
.topNav{
	width: 95%;
	height: 0.5rem;
	background: #fff;
	border-radius: 6px;
	margin: 0 auto;
	display: flex;
	justify-content: space-around;
	padding-top: 0.05rem;
	position: relative;
	/* top: -10%; */
	z-index: 10;
	margin-top: -7%;
	box-shadow: 0rem 0rem 0.05rem 0.01rem #ccc;
}
.topNav p{
	font-size: 12px;
	color: #2f2f2f;
	/* margin-top: 0.08rem; */
	margin: 0 auto;
}
.topNav span{
	display: block;
	width: 0.28rem;
	height: 0.28rem;
	margin: 0 auto;
	background-image: url(../assets/img/home-fivemain-sprite2x@v7.15.png);
	background-repeat: no-repeat;
	background-size: 0.28rem;
}
.topNav :nth-child(1) span{
	background-position:  0px 0px;
}
.topNav :nth-child(2) span{
	background-position:  0px -0.28rem;
}
.topNav :nth-child(3) span{
	background-position:  0px -0.55rem;
}
.topNav :nth-child(4) span{
	background-position:  0px -0.84rem;
}
.topNav :nth-child(5) span{
	background-position:  0px -1.12rem;
}
</style>
