<template>
  <div id="app">
    <DisplayDataRespondToEvents/>
  </div>
</template>

<script>
import DisplayDataRespondToEvents from './components/DisplayDataRespondToEvents'

export default {
  name: 'app',
  components: {
    DisplayDataRespondToEvents
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
