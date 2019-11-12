<!--
 * @Author: yx
 * @Date: 2019-11-09 15:32:58
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 15:54:31
 * @Description: 底部
 -->


 <template>
  <footer>
       <ul>
            <li>
                <router-link to='/Index' v-on:click="clk" v-bind:style="col">
                    <span class="el-icon-s-home"></span>
                    <p>首页</p>
                </router-link>
            </li>
            <li>
                <router-link to='/Index'>
                    <span class="el-icon-date"></span>
                    <p>行程</p>
                </router-link>
            </li>
            <li>
                <router-link to='/Index'>
                    <span class="el-icon-camera"></span>
                    <p>旅拍</p>
                </router-link>
            </li>
            <li>
                <router-link to='/CustService'>
                    <span class="el-icon-headset"></span>
                    <p>客服</p>
                </router-link>
            </li>
            <li>
                <router-link to='/Index'>
                    <span class="el-icon-user"></span>
                    <p>我的</p>
                </router-link>
            </li>
        </ul>
  </footer>
</template>

<script>

export default {
    name: 'MyFooter',
    data() {
        return {
           col:'color:rgb(47, 123, 221)'
        }
    },
    methods: {
        clk:function(){
            // let obj = document.getElementsByTagName('li').children;
            // console.log('obj');
            
        }
    },
}
</script>

<style>
footer{
  margin: 0 auto;
  width:100%;
  height: .5rem;
  background-color:#fff;
  position: fixed;
  bottom: 0;
  border-top: 1px solid #ccc;
}
ul{
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 100%;
}
ul li{
    width: 25%;
    height: 100%;
    text-align: center;
}
ul li a{
    color: black;
}
ul span{
   font-size: 0.18rem;
   margin: 0.04rem 0;
}

</style>
