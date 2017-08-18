<template>
  <div class="container">
    <div class="thief"></div>
    <h2>{{ name }}</h2>

    <div v-for="(stat, value) in stats" class="stats">
      {{value}}: {{ stat }}
    </div>
  </div>
</template>

<script>
import './Thief.scss'

export default {
  name: 'thief',
  data () {
    return {
      name: 'Thief',
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
