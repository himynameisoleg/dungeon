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
import './Archer.scss'

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
