<template>
  <div>
    <div id="app">
      <boo></boo>
      <div class="tabletop">

        <!-- characters -->
        <!-- <archer class="character"></archer>
        <mage class="character""></mage>
        <priest class="character"></priest>
        <thief class="character"></thief>
        <warrior class="character"></warrior> -->
        <prototype class="character"></prototype>

        <!-- lands -->
        <swamp class="land"></swamp>
        <div class="monster"><h2>Monzter</h2></div>

        <div class="box" @click="random()"></div>
      </div>

    </div>

  </div>
</template>

<script>
import Boo from './components/Boo'
//import characters
import Prototype from './components/characters/Prototype'

import Archer from './components/characters/Archer'
import Mage from './components/characters/Mage'
import Priest from './components/characters/Priest'
import Thief from './components/characters/Thief'
import Warrior from './components/characters/Warrior'
//import lands
import Forest from './components/lands/Forest'
import Island from './components/lands/Island'
import Mountain from './components/lands/Mountain'
import Plaines from './components/lands/Plaines'
import Swamp from './components/lands/Swamp'


export default {
  name: 'app',
  data () {
    return {
      isChosen: 0,
    }
  },
  components: {
    Boo,
    Prototype,
    Archer,
    Mage,
    Priest,
    Thief,
    Warrior,
    Forest,
    Island,
    Mountain,
    Plaines,
    Swamp
  },
  methods: {
    log: function () {
      console.log(this.isChosen);
    },
    random: function () {
      this.isChosen = Math.floor(Math.random()*5);
      this.log();
    }
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
.hidden {
  display: none;
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
.box {
  height: 20px;
  width: 20px;
  background-color: black;
  position: absolute;
}
</style>
