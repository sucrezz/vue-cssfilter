<template>
  <div id="app">
    <header class="flex">
      <span>项目基于Vue框架：</span>
      <div>
        <img alt="Vue logo" src="./assets/logo.png">
      </div>
    </header>
    <section>
      <index />
    </section>
  </div>
</template>

<script>
import index from './components/index/index'

export default {
  name: 'app',
  components: {
    index
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
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
  #app header{
    width: 100%;
    height: 60px;
    line-height: 60px;
    padding: 0 5%;
  }
  #app header img{
    width: 30px;
    height: 30px;
    vertical-align: middle;
  }
  #app section{
    width: 100%;
    padding: 0 5%;
  }
</style>
