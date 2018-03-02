<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <li v-for="mach in machines"><a href="#">
      {{mach.machines}}
    </a></li>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'List of Coffee Machines',
      machines: [
        {machines: 'Machine1'},
        {machines:'Machine2'},
        {machines:'Machine3'}
      ],
      methods: {
        active: function(){
          console.log(status);
        }
      }
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
