<template>
  <div id="app">
    <boo></boo>
    <div class="tabletop">
      <archer class="character"></archer>
      <swamp class="land"></swamp>
      <div class="monster"><h2>Monzter</h2></div>
    </div>

  </div>
</template>

<script>
import Boo from './components/Boo'
import Archer from './components/characters/Archer'
import Swamp from './components/lands/Swamp'

export default {
  name: 'app',
  components: {
    Boo,
    Archer,
    Swamp
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
  margin-top: 20px;
}
.tabletop {
  position: absolute;
  left: 0;
  right: 0;
  margin: auto;
  width: 100%;
  height: 320px;
  background-color: #EEEEEE;
  border-top: 1px solid #424242;
  display: inline-block;
  padding: 20px;
}
.character {
  float: left;
}
.land{
  float: left;
}
.monster {
  float: left;
  width: 180px;
  height: 280px;
  padding: 20px;
  background-color: #ccc;
}
</style>
