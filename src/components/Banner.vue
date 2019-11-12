<!--
 * @Author: yx
 * @Date: 2019-11-08 20:15:07
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 09:31:39
 * @Description: 轮播图
 -->

<template>
  <div class="swiper-container">
    <div class="swiper-wrapper">
        <div class="swiper-slide"><img src="../assets/img/zg0i19000001621350E3B.jpg" alt=""></div>
        <div class="swiper-slide"><img src="../assets/img/zg07190000017lin0DB8B.jpg" alt=""></div>
        <div class="swiper-slide"><img src="../assets/img/zg0s180000014rym6B157.jpg" alt=""></div>
        <div class="swiper-slide"><img src="../assets/img/zg0n190000017xvzmC042.jpg" alt=""></div>
    </div>
     <!-- <div class="swiper-pagination"></div>
     <div class="swiper-pagination"></div>
     <div class="swiper-pagination"></div>
     <div class="swiper-pagination"></div> -->
</div>
</template>

<script>
import Swiper from 'swiper';
export default {
  name: 'Banner',
  data () {
    return {
     imgs:[]
    }
  },
  methods: {
      
  },
}
window.onload =function(){
    let mySwiper = new Swiper('.swiper-container',{
        autoplay:true,
        speed:300,
        grabCursor:true,
        loop : true
    });
}
  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url(https://unpkg.com/swiper/css/swiper.css);
.swiper-container{
    width: 100%;
	height: 1.36rem;
  /* margin-top: .35rem; */
  
}
.swiper-container .swiper-pagination{
    width: 0.1rem;
    height: 0.1rem;
    background: red;
    z-index: 10;
}
img{
    /* display: block; */
    width: 100%;
	height: 100%;
	border-bottom-left-radius: 12px;
	border-bottom-right-radius: 12px;
}
</style>
