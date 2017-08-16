<template>
  <div class="container">
    <div class="archer"></div>
    <h2>{{ name }}</h2>

    <div v-for="(stat, value) in stats" class="stats">
      {{value}}: {{ stat }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'archer',
  data () {
    return {
      name: 'Archer',
      stats: {
        health: 10,
        agility: 1,
        strength: 1,
        mana: 1,
        dextarity: 4
      }
    }
  },
  methods: {


  },
  computed: {

  }
}
</script>

<style scoped>
.container {
  width: 200px;
  height: 320px;
  border: 1px solid white;
  padding: 10px;
  background-color: #ccc;
}
.archer {
  width: 30px;
  height: 30px;
  border: 1px solid white;
  background-color: #00C858;
  margin-bottom: 20px;
  float: left;
}
.stats {
  border-top: 1px solid black;
  text-align: left;
}

</style>
