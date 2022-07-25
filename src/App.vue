<template>
  <div id="app">
    <div class="container">
      <Barra />
    </div>
  </div>
</template>

<script>
import Barra from "./components/Barra.vue";

export default {
  name: "App",
  components: {
    Barra,
  },
};
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
