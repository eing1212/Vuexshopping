<template>
  <header>
    <b-navbar
        toggleable="lg"
        type="dark"
        variant="warning"
        class="mb-4"
      >
        <b-navbar-brand href="#">ZenShop</b-navbar-brand>
        <span class="navbar-brand mb-0 h1">
          <span> | </span>
        Cart <span class="badge badge-secondary">{{ totalQty }}</span>
      </span>
      </b-navbar>

      
    
  </header>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  name: "Header",
  computed: {
    ...mapGetters(["cart"]),
    totalQty() {
      return this.cart.reduce((a, b) => a + b.qty, 0);
    },
  },
};
</script>

<style scoped>
header {
  margin-bottom: 10vh;
}
</style>
