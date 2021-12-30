<template>
  <div id="app">
    <img src="./assets/logo.png">
    <CarCarousel/>
    <Hexagon/>
    <HelloWorld/>
  </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld'
    import CarCarousel from "./components/CarCarousel";
    import Hexagon from "./components/Hexagon";

    export default {
        name: 'App',
        components: {
            HelloWorld, CarCarousel, Hexagon
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
