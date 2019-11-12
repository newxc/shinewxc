<!--
 * @Author: yx
 * @Date: 2019-11-08 22:31:20
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 14:16:53
 * @Description: 
 -->

 <template>
  <div>
     <div class="tripNav">
        <div class="bigNav">
            <a href="#">
            <img src="../assets/img/跟团游.png" alt="">
                <p>跟团游</p>
            </a>
            <a href="#">
                <img src="../assets/img/自由行.png" alt="">
                <p>自由行</p>
            </a>
            <a href="#">
                <img src="../assets/img/定制旅行.png" alt="">
                <p>定制旅游</p>
            </a>
            <a href="#">
                <img src="../assets/img/私家团.png" alt="">
                <p>私家团</p>
            </a>
            <a href="#">
                <img src="../assets/img/邮轮旅行.png" alt="">
                <p>邮轮游</p>
            </a>
        </div>
        <div class="smallNav">
            <a href="#">
                <img src="../assets/img/周边游.png" alt="">
                <p>周边游</p>
            </a>
            <a href="#">
                <img src="../assets/img/300a13000000tztb283AD.png" alt="">
                <p>一日游</p>
            </a>
            <a href="#">
                <img src="../assets/img/300l10000000pj3oq76D9.png" alt="">
                <p>景点·门票</p>
            </a>
            <a href="#">
                <img src="../assets/img/鸿鹄·奢游.png" alt="">
                <p>鸿鹄·奢游</p>
            </a>
            <a href="#">
                <img src="../assets/img/300713000000uf6gaA365.png" alt="">
                <p>当地向导</p>
            </a>
            <a href="#">
                <img src="../assets/img/300b11000000ricm57816.png" alt="">
                <p>主题旅游</p>
            </a>
            <a href="#">
                <img src="../assets/img/300d13000000tx0nbB454.png" alt="">
                <p>亲子·游学</p>
            </a>
            <a href="#">
                <img src="../assets/img/300h13000000vjqbpE86C.png" alt="">
                <p>海岛</p>
            </a>
            <a href="#">
                <img src="../assets/img/300j13000000ty0js75C3.png" alt="">
                <p>带娃出游</p>
            </a>
            <a href="#">
                <img src="../assets/img/300q13000000twl3sEC5D.png" alt="">
                <p>浪漫之旅</p>
            </a>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TripNav',
  data() {
      return {
         
      }
  }
}
</script>

<style>
.tripNav{
	width: 95%;
	overflow: hidden;
	margin: 0 auto;
    margin-bottom: 0.17rem;
}
.tripNav a{
    display: block;
    width: 20%;
    /* height: 0.35rem; */
    text-align: center;
    color: black;
}
.tripNav a span{
    display: block;
    width: 0.25rem;
	height: 0.25rem;
    overflow: hidden;
    margin: 0 auto;
}
.tripNav p{
    font-size: 12px;
    line-height: 12px;
}
.bigNav{
    display: flex;
	justify-content: space-around;
}
.bigNav img{
    width: 0.6rem;
    height: 0.6rem;
}
.smallNav{
    display: flex;
	justify-content: space-around;
    flex-wrap: wrap;
}
.smallNav img{
    width: 0.5rem;
    height: 0.5rem;
}
</style>
