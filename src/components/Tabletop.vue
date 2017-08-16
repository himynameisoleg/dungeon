<template>
  <div class="container">
    <div class="row">

      <div class="col-boxes">
        <div class="player el-light" id="el-light" @click="addLight()">
          <span> {{ points.light }} </span>
        </div>
        <div class="player el-dark" id="el-dark" @click="addDark()">
          <span> {{ points.dark }} </span>
        </div>
        <div class="player el-fire" id="el-fire" @click="addFire()">
          <span> {{ points.fire }} </span>
        </div>
        <div class="player el-water" id="el-water" @click="addWater()">
          <span> {{ points.water }} </span>
        </div>
        <div class="player el-grass" id="el-grass" @click="addGrass()">
          <span> {{ points.grass }} </span>
        </div>
      </div>

    </div>

    <h1> {{ totalPoints }} </h1>
    <div class="boss">
      {{ createBoss }}
    </div>
    <h1> {{ results }} </h1>

  </div>
</template>

<script>
export default {
  name: 'tabletop',
  data () {
    return {
      victory: 'you are victorious!',
      death: 'you are dead!',
      points: {
        light: 0,
        dark: 0,
        fire: 0,
        water: 0,
        grass: 0
      },
      total: 0,
    }
  },
  methods: {
    addLight: function () {
      this.points.light++;
    },
    addDark: function () {
      this.points.dark++;
    },
    addFire: function () {
      this.points.fire++;
    },
    addWater: function () {
      this.points.water++;
    },
    addGrass: function () {
      this.points.grass++;
    },
  },
  computed: {
    totalPoints: function () {
      this.total = this.points.light + this.points.dark + this.points.fire + this.points.water + this.points.grass;
      return this.total;
    },
    createBoss: function () {
      if (this.total = 20) {
        var boss = Math.floor(Math.random() * 20);
        return boss;
      }
    },
    results: function () {
      if (this.points.fire === 10) {
        return this.victory;
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  width: 400px;
  height: 300px;
  padding: 20px;
  background-color: #1D1D1D;

  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: white;
  font-size: 1em;

}
.row {
  /*display: inline-block;*/
}
.col-boxes {
  float:left;
  margin-right: 4px;
  /*display: inline-block;*/
}

.player {
  width: 30px;
  height: 30px;
  border: 1px solid white;
  margin-bottom: 4px;
  cursor: pointer;
  display: inline-block;
}
.player:hover {
  opacity: 0.7;
}

.el-light {
  background-color: #FFC975
}
.el-dark {
  background-color: #A8A39B;
}
.el-fire {
  background-color: #FF6427;
}
.el-water {
  background-color: #0093C4;
}
.el-grass {
  background-color: #00C858;
}

.boss {
  width: 60px;
  height: 60px;
  background-color: red;
  border: 1px solid white;
  float: left;
}

</style>
