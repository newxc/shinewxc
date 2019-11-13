<!--
 * @Author: yx
 * @Date: 2019-11-09 15:32:58
 * @LastEditors: yx
 * @LastEditTime: 2019-11-13 14:17:06
 * @Description: 底部
 -->


 <template>
  <footer>
       <ul>
           <li v-for="(item,index) in lis" :key="index"  @click="clk(index)"  >
               <router-link  v-bind:class="{blue:isblue[index]}" :to="item.rot" >
                   <!-- :class="isactive==index?'addclass':''" -->
                    <span :class="item.cls"></span>
                    <p>{{item.navName}}</p>
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
        //    col:'color:rgb(47, 123, 221)',
           lis:[
               {
                   "rot":"/Index",
                   "cls":"el-icon-s-home",
                   "navName":"首页",
               },
               {
                   "rot":"/Index",
                   "cls":"el-icon-date",
                   "navName":"行程"
               },
               {
                   "rot":"/Index",
                   "cls":"el-icon-camera",
                   "navName":"旅拍"
               },
               {
                   "rot":"/CustService",
                   "cls":"el-icon-headset",
                   "navName":"客服"
               },
               {
                   "rot":"/Index",
                   "cls":"el-icon-user",
                   "navName":"我的"
               }
           ],
           isblue:[
               true,false,false,false,false
           ]
        //    isactive:0
        }
    },
    methods: {
        clk(index){
            console.log(this.isblue[index])
            for(let i in this.isblue){
                this.isblue[i] = false;
            }
            
            this.isblue[index] = true;
            console.log(this.isblue[index])
        }
    },
    created() {
        
    },
}
</script>

<style scoped>
footer{
  margin: 0 auto;
  width:100%;
  height: .5rem;
  background-color:#fff;
  position: fixed;
  bottom: 0;
  border-top: 1px solid #ccc;
  z-index: 20;
}
.blue{
    color:rgb(47, 123, 221);
}
/* .black{
    color: black;
} */
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
