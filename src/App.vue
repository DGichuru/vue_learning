<template>
  <div id="app">
    <h1>Fetch Data with API </h1>
    <Employee />
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Employee from './components/Employee.vue'

export default {
  name: 'App',
  components: {
    
    Employee
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
