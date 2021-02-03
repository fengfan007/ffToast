<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>

    <button @click="handleClick">点击触发toast</button>

    <test-toast ref="toast"></test-toast>

  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    handleClick() {
      this.$nextTick( () => {
        this.$refs.toast.toastPlugin('哎呀，我被触发了！' , 3000)
      })
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
</style>
