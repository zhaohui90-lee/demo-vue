<template>
  <div class="page1">
    <div>
      <h2>{{msg1}}</h2>
      <h3>{{msg3}}</h3>
    </div>
    <div class="methods" @click="getDetailInfo()">点击测试</div>
    <div class="show" @click="change()">{{msg4}}</div>
    <h1 v-if="seen">vue条件</h1>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'page1',
  data () {
    return {
      msg: '忘却的旋律',
      msg1: 'bkbkjbkbk',
      msg3: 'nnciaosncianoi',
      msg4: '点击显示隐藏内容',
      msg5: '点击,会反转的消息',
      seen: false
    }
  },
  methods: {
    change () {
      this.seen = this.seen !== true
      this.msg4 = this.msg4 === '点击隐藏显示内容' ? '点击显示隐藏内容' : '点击隐藏显示内容'
    },
    getDetailInfo () {
      axios
        .get('./HelloWorld.vue')
        .then(this.getMsgInfo)
        .catch(this.getErrorInfo)
    },
    getMsgInfo (res) {
      console.log('success')
    },
    getErrorInfo (res) {
      console.log('error')
    }
  }
}
</script>

<style scoped>

h1{
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  color: chocolate;
}
h2,h3{
  color: brown;
}
</style>
