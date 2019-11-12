<!--
 * @Author: yx
 * @Date: 2019-11-09 15:32:58
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 17:40:48
 * @Description: 底部
 -->


 <template>
<div class="tips">
    <div class="tipstop"></div>
    <div class="tipscon">
        <h4>旅行贴士</h4>
        <ul>
            <li>
                <img src="../assets/img/c1.png" alt="">
                <p>旅行指南</p>
                <span>轻松解决旅行难题</span>
            </li>
            <li>
                <img src="../assets/img/c2.png" alt="">
                <p>航班发生延误处理</p>
                <span>飞机延误退改指南</span>
            </li>
            <li>
                <img src="../assets/img/c3.png" alt="">
                <p>锁定飞机号座位</p>
                <span>在线选座快人一步</span>
            </li>
            <li>
                <img src="../assets/img/c4.png" alt="">
                <p>同行驴友互助交流</p>
                <span>轻松解决旅行难题</span>
            </li>
        </ul>
    </div>
    <div class="travel">
        <h4>出行当地服务</h4>
        <div class="traCon">
            <a href="#">
                <img src="../assets/img/t1.png" alt="">
                <span>紧急支援</span>
            </a>
            <a href="#">
                <img src="../assets/img/t6.png" alt="">
                <span>出行清单</span>
            </a>
            <a href="#">
                <img src="../assets/img/t7.png" alt="">
                <span>微领队</span>
            </a>
            <a href="#">
                <img src="../assets/img/t8.png" alt="">
                <span>翻译</span>
            </a>
        </div>
    </div>
    <div class="complaints">
        <h4>我的投诉</h4>
        <div class="complaintsCon">
            暂无进行中的投诉
        </div>
    </div>
    <div class="ishelp">
        <p></p>
    </div>
</div>
</template>

<script>

export default {
    name: 'Tips',
    data() {
        return {
           
        }
    },
    methods: {
        clk:function(){
            
            
        }
    },
}
</script>

<style>
.tipstop{
    width: 100%;
    height: 1.36rem;
    background: #008cf7;
    border-bottom-left-radius: 12px;
	border-bottom-right-radius: 12px;
}
.tipscon{
    width: 95%;
    margin: 0 auto;
    background: #fff;
    box-shadow: 0rem 0rem 0.1rem 0.01rem #ccc;
    z-index: 10;
    position: relative;
    margin-top: -19%;
    padding:  0 2%;
    box-sizing: border-box;
    border-radius: 0.07rem;
}
.tipscon h4{
    font-size: 0.16rem;
    line-height: 0.4rem;
    font-weight: normal;
    border-bottom: 1px solid #ddd;
    margin-bottom: 0.1rem;
}
.tipscon ul{
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
}
.tipscon ul li{
    width: 46%;
    height: 1.5rem;
    text-align: left;
}
.tipscon ul li img{
    width: 100%;
}
.tipscon ul li p{
    font-size: 0.14rem;
    line-height: 0.24rem;
}
.tipscon ul li span{
   font-size: 0.12rem;
   color: #aaa;
}
.travel{
    width: 95%;
    margin: 0 auto;
    background: #fff;
    box-shadow: 0rem 0rem 0.1rem 0.01rem #ccc;
    box-sizing: border-box;
    border-radius: 0.07rem;
     padding:  0 2% 0.15rem;;
     margin-top: 0.1rem;
}
.travel h4{
     font-size: 0.16rem;
    line-height: 0.4rem;
    font-weight: normal;
    width: 100%;
    border-bottom: 1px solid #ddd;
}
.traCon{
    display: flex;
    justify-content: space-around;
}
.traCon a{
    color: black;
    padding-top: 0.1rem;
}
.traCon img{
    width: 0.3rem;
    height: 0.3rem;
    display: block;
}
.traCon span{
    font-size: 0.12rem;
}
.complaints{
    width: 95%;
    margin: 0 auto;
    background: #fff;
    box-shadow: 0rem 0rem 0.1rem 0.01rem #ccc;
    box-sizing: border-box;
    border-radius: 0.07rem;
     padding:  0 2% 0.15rem;;
     margin-top: 0.1rem;
     margin-bottom: 1rem;
}
.complaints h4{
    font-size: 0.16rem;
    line-height: 0.4rem;
    font-weight: normal;
    border-bottom: 1px solid #ddd;
    margin-bottom: 0.1rem;
}
.complaintsCon{
    text-align: center;
    line-height: 0.5rem;
    font-size: 0.12rem;
    color: #bbb;
}
</style>
