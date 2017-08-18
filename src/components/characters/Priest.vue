<template>
  <div class="container">
    <div class="priest"></div>
    <h2>{{ name }}</h2>

    <div v-for="(stat, value) in stats" class="stats">
      {{value}}: {{ stat }}
    </div>
  </div>
</template>

<script>
import './Priest.scss'

export default {
  name: 'priest',
  data () {
    return {
      name: 'Priest',
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
