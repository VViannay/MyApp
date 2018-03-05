<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <h3>Display Or Hide Machine Inactive</h3>
    <toggle-button v-model="hideInactiveMachine"labels="false"/>
    <p>Use the Toggle for active/desactive:</p>
    <li  v-for="mach in machines" v-show="!hideInactiveMachine || mach.active">
      <toggle-button v-model="mach.active" labels="false"/>
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
      hideInactiveMachine: true,
      machines: [
        {machines: 'Nesspresso Coffee',
         active: true,

        },
        {machines: 'Royal  Coffee',
         active:false,
        },

        {machines: 'Tassimo Coffee',
          active: true,

        },

        {machines: 'Senseo Coffee',
          active: true,

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
