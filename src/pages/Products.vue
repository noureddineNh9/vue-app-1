<template>
  <div class="p-5">
    <div v-if="loading">
      <h1 class="text-center">loading</h1>
    </div>
    <div v-else>
      <div class="card-container">
        <div :key="product.id" v-for="product in products">
          <Card :product="product" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "../components/Card.vue";

export default {
  name: "Products",
  components: {
    Card: Card,
  },
  data() {
    return {
      products: Array,
      loading: true,
    };
  },
  methods: {
    async getAllProducts() {
      const res = await fetch("https://fakestoreapi.com/products");
      const products = await res.json();
      this.products = products;
      this.loading = false;
      console.log(products);
    },
  },
  created() {
    this.getAllProducts();
  },
};
</script>
