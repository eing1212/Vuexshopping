<template>
  <b-row>
    <b-card
      style="width: 15rem;"
      v-for="item in products"
      :key="item.id"
    >
      <img :src="item.imgUrl" class="card-img-top" :alt="item.title" />
      <b-card-body>
        <p class="card-title">{{ item.title }}</p>
        <p class="card-text">$ {{ item.price.toLocaleString() }}</p>
        <b-button class="btn btn-primary" @click="addItemToCart(item)">
          Add to cart
        </b-button>
      </b-card-body>
    </b-card>
  </b-row>
</template>

<script>
import { mapActions, mapGetters } from "vuex";

export default {
  name: "Shop",
  mounted() {
    this.getProducts();
  },
  computed: {
    ...mapGetters(["products"]),
  },
  methods: {
    ...mapActions(["addItemToCart", "getProducts"]),
  },
};
</script>

<style scoped>
.card {
  padding: 20px;
  border-block-color: #ac4848
  
}
</style>
