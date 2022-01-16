<template>
  <Layout02></Layout02>
</template>

<script>
    import Layout01 from "./components/eleui/Layout01";
    import Layout02 from "./components/eleui/Layout02";

    export default {
        name: 'App',
        components: {
            Layout01, Layout02
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
