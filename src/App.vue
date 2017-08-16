<template>
  <div id="app">
    <boo></boo>
    <tabletop id="tabletop"></tabletop>
  </div>
</template>

<script>
import Boo from './components/Boo'
import Tabletop from './components/Tabletop'

export default {
  name: 'app',
  components: {
    Boo,
    Tabletop
  }
}
</script>

<style>
* {
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#tabletop {
  position: absolute;
  left: 0;
  right: 0;
  margin: auto;
}
</style>
