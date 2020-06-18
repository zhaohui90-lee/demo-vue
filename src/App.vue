<template>
  <div id="app">
    <div class="head P-left">
      <img src="./assets/head.png">
    </div>
    <div class="baseInfo">
      <h1 id="nickName">{{nickName}}</h1>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      nickName: '忘却的旋律'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.head{
  float: left;
  width: 7rem;
  margin-left: 0.1rem
}
.baseInfo{
  float: left;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 10px;
  margin-top: 0px;
}
</style>
