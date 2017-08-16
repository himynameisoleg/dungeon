<template>
  <div id="app">
    <boo></boo>
    <tabletop id="tabletop"></tabletop>
    <archer id="archer"></archer>
    
  </div>
</template>

<script>
import Boo from './components/Boo'
import Tabletop from './components/Tabletop'
import Archer from './components/characters/Archer'

export default {
  name: 'app',
  components: {
    Boo,
    Tabletop,
    Archer
  }
}
</script>

<style>
/** {
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}*/
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
#tabletop {
  position: absolute;
  left: 0;
  right: 0;
  margin: auto;
}
#archer {
  position: absolute;
}
</style>
