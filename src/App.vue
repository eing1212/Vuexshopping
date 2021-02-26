<template>
  <div id="app">
    <Header />
    <div class="main">
      <b-container>
        <b-row>
          <b-col class="col-8"><Shop /></b-col>
          <b-col class="col-4"><Cart /></b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import Shop from "./components/Shop";
import Cart from "./components/Cart";

export default {
  name: "App",
  components: {
    Shop,
    Header,
    Cart,
  },

    Cart};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: rgb(219, 207, 253);
}
</style>
