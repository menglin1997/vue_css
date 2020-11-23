<!--
 * @Descripttion: 
 * @version: 
 * @Author: zml
 * @Date: 2020-08-11 10:19:22
 * @LastEditors: zml
 * @LastEditTime: 2020-08-11 11:03:56
-->
<template>
  <h1>{{ msg }}</h1>
  <button @click="count++">count is: {{ count }}</button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>

  
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  
  data() {
    return {
      count: 0,
      color:'red'
    }
  },
  mounted() {
    setInterval(() => {
      this.color = this.color === 'red' ? 'skyblue' : 'red'
    }, 500);
  },
}
</script>
<style scoped vars = '{ color }'>
  h1 {
    color: var(--color)
  }
</style>