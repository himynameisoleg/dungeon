<template>
  <div class="boo">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'boo',
  data () {
    return {
      msg: 'DUNGEON'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: bold;
  color: #424242;
}
</style>
