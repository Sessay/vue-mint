<template>
  <div id="app">
    <div id="nav">
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> -->
      <mt-button type="default" @click="test">default</mt-button>
      <mt-button type="primary">primary</mt-button>
      <mt-button type="danger">danger</mt-button>
    </div>
    <router-view/>
  </div>
</template>
<script>
import { Toast } from 'mint-ui'
export default {
  methods: {
    test () {
      Toast({
        message: '提示',
        position: 'bottom',
        duration: 5000
      })
    }
  }
}
</script>

<style lang="less">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
