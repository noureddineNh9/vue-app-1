<template>
  <div class="bg-gray-200 p-4 flex justify-between">
    <router-link to="/"><img src="../img/Logo.svg" alt="" /></router-link>
    <router-link to="/about">About</router-link>
    <router-link to="/products">Products</router-link>
  </div>
</template>

<script>
export default {
  name: "home",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
    };
  },
};
</script>
