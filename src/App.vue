<template>
  <div id="app">
   <p>{{msg}}</p>
   <Content v-bind:weather_data="weather_data"></Content>
  </div>
</template>

<script>
import Content from './components/Content.vue';

export default {
  name: 'app',
   components: {
    'Content': Content
  },
  data () {
    return {
      msg: 'Vue js application',
      weather_data: {
        location: "California",
        temperature: {
          current: "35 C",
        },
        highlights: {
          uvindex: "3",
          windstatus: {
            speed: "20 km/h",
            direction: "N-E",
          },
          visibility: "12 km",
        },
      },
    }
  },
  methods: {

  },
  computed: {
    
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
