<!--
 * @Author: yx
 * @Date: 2019-11-09 20:09:14
 * @LastEditors: yx
 * @LastEditTime: 2019-11-11 19:48:09
 * @Description: 返回
 -->

<template>
    <div class="back">
         <!--左箭头-->  
         <span class="el-icon-arrow-left"  @click="back()" ></span>
    </div>  
</template>

<script>

export default {
  name: 'Back',
  data () {
    return {
      
    }
  },
  methods:{
      back(){
          this.$router.go(-1);
      }
  }
}
</script>

<style scoped>
.back{
    width: 10%;
    float: left;
}
.back span{
    font-size: 0.2rem;
}

</style>
