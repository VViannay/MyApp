<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <p>Use the checkbox for active/desactive:</p>
    <li v-for="mach in machines">
      <input v-model="mach.active" type="checkbox">
      <h3 :class="{inactive: !mach.active}">{{mach.machines}}</h3>
    </li>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: function () {
    return {
      msg: 'List of Coffee Machines',
      machines: [
        {machines: 'Nesspresso Coffee :',
         active: true
        },
        {machines: 'Moulinex Coffee :',
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

li {
  color: #42b983;
}
  .inactive {
    color: dimgrey;
  }
</style>
