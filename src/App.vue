<!--
 * @Author: yx
 * @Date: 2019-11-08 18:01:56
 * @LastEditors: yx
 * @LastEditTime: 2019-11-08 22:23:18
 * @Description: 
 -->
<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
html{
  font-size: 26.67vw;
  height:100%;
}
body{
  font-size: 14px;
  height: 100%;
}
#app { 
  margin-top: 5px;
}
ul,li{
  list-style: none;
}
a{
  text-decoration: none;
}
</style>
