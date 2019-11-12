<!--
 * @Author: yx
 * @Date: 2019-11-11 19:50:46
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 20:21:15
 * @Description: 定位头部
 -->

<template>
    <div class="posTop">
        <Back></Back>
        <input type="text" placeholder="全球城市(如北京/beijing/bj)">
        <div class="posBot">
            <span>境内·港澳台</span>
            <span>境外</span>
        </div>
    </div>  
</template>

<script>
import Back from './Back';
export default {
  name: 'PosTop',
  data () {
    return {
      msg:""
    }
  },
  components:{
      Back
  }
}
</script>

<style scoped>

.posTop{
    width: 100%;
    margin: 0 auto;
    height: .6rem;
    /* overflow: hidden; */
    background: #fff;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 20;
    padding: 0.1rem 0.12rem 0;
    box-shadow: 0rem 0rem 0.05rem 0.01rem #ccc;
}
.posTop input{
    width: 80%;
	height: 0.22rem;
	background: #eee;
    padding-top: 0.02rem;
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
.posBot{
    width: 100%;
    /* height: 0.32rem; */
    display: flex;
    justify-content: space-around;
    line-height: 0.35rem;
}
.posBot :first-child{
    border-bottom: 2px solid rgb(26, 93, 238);
}
</style>
