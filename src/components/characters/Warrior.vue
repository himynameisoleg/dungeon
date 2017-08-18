<template>

  <div class="container">
    <div class="warrior"></div>
    <h2>{{ name }}</h2>

    <div v-for="(stat, value) in stats" class="stats">
      {{value}}: {{ stat }}
    </div>
  </div>
</template>

<script>
import './Warrior.scss'

export default {
  name: 'warrior',
  data () {
    return {
      name: 'Warrior',
      stats: {
        health: 10,
        agility: 1,
        strength: 1,
        mana: 4,
        dextarity: 1
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
</style>
