<template>
  <div class="container">
    <div class="prototype"></div>
    <h2>{{ name }}</h2>

    <div v-for="(stat, value) in stats" class="stats">
      {{value}}: {{ stat }}
    </div>
  </div>
</template>

<script>
import './Prototype.scss'

export default {
  name: 'prototype',
  data () {
    return {
      name: '',
      stats: {
        health: 0,
        agility: 0,
        strength: 0,
        mana: 0,
        dextarity: 0
      }
    }

  },
  methods: {
    
  },
  computed: {
    getCharName: function() {
      let names = ['Archer', 'Mage', 'Priest', 'Thief', 'Warrior'];
      this.name = names[Math.floor(Math.random()*names.length)]
    },
    getCharStats: function() {
      this.stats.health = Math.floor(Math.random()*10) + 5;
      this.stats.agility = Math.floor(Math.random()*10) + 1;
      this.stats.strength = Math.floor(Math.random()*10) + 1;
      this.stats.mana = Math.floor(Math.random()*10) + 1;
      this.stats.dextarity = Math.floor(Math.random()*10) + 1;
    }
  },
  created: function () {


    this.getCharName();

    this.getCharStats();


  }
}
</script>
