<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <li v-for="mach in machines"><a href="#">
      {{mach.machines}}
      {{mach.active}}
      <input v-model="mach.active" type="checkbox">
    </a></li>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: function () {
    return {
      msg: 'List of Coffee Machines',
      machines: [
        {machines: 'Machine1',
         active: true
        },
        {machines: 'Machine2',
         active:false
        },

      ],

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
  list-style: none;
  
  margin: 50px;
}

a {
  color: #42b983;
}
</style>
