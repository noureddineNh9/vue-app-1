<template>
  <div class="card">
    <img :src="product.image" alt="" class="h-40 w-40" />
    <h3>{{ product.title }}</h3>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    product: Object,
  },
};
</script>
