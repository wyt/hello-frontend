<template>
  <div id="app">
    <Honeycomb></Honeycomb>
  </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld'
    import CarCarousel from "./components/CarCarousel";
    import Hexagon from "./components/Hexagon";
    import Honeycomb from "./components/Honeycomb";

    export default {
        name: 'App',
        components: {
            HelloWorld, CarCarousel, Hexagon, Honeycomb
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
