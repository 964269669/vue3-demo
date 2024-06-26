<template>
  <div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age }}</h2>
    <button @click="changeName"> 修改名字</button>
    <button @click="changeAge"> 修改年龄</button>
    <button @click="showTel"> 查看联系方式</button>
  </div>
</template>

<script lang="ts">
  export default {
    name: 'Person',
    setup() {
      // 数据
      let name= 'zhang san'
      let age = '18'
      let tel = '121212121'


      // 方法
      const changeName = () => {
        name = 'wang wang'
      }
      const changeAge = () => {
        age = '20'
      }
      const showTel = () => {
        alert(tel)
      }
      return {
        name, age, tel, changeName, changeAge, showTel
      }
    }
  }

</script>

<style lang="scss" scoped>

</style>