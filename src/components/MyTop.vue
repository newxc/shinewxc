<!--
 * @Author: yx
 * @Date: 2019-11-09 20:09:14
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 19:47:40
 * @Description: 返回
 -->

<template>
    <div class="myTop">
        <Back></Back>
        <!--左箭头-->  
        <span>{{msg}}</span>
        <router-link to="/CustService"><span class="el-icon-chat-line-round"></span></router-link>
        <router-link to="/CustService"><span class="el-icon-headset"></span></router-link>
    </div>  
</template>

<script>
import Back from './Back';
export default {
  name: 'MyTop',
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

.myTop{
    width: 100%;
    margin: 0 auto;
    height: .2rem;
    background: rgba(255,255,255,.8);
    position: fixed;
    top: 0;
    left: 0;
    z-index: 20;
    padding: 0.1rem 0.12rem;
}
.myTop a{
    float: right;
}
.myTop a{
    color: black;
    font-size: 0.18rem;
    /* float: left; */
}
.myTop :nth-child(2){
    margin-left: 35%; 
    font-size: 0.16rem;
}
.myTop :nth-child(3){
    float: right;
    margin-right: 9%; 
}
.myTop :nth-child(4){
    float: right;
    margin-right: 4%; 
}
</style>
