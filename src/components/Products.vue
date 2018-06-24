<template>
  <div class="Products">
    <Product
      v-for="product in products"
      v-bind:title="product.title"
      v-bind:description="product.description"
      v-bind:youtube="product.youtube"
      :key="product.text"
    />
  </div>
</template>

<script>
import Product from './Product';

export default {
  name: 'Products',
  components: { Product },
  data: () => {
    return {
      products: require('../data/products.json'),
    };
  },
};
</script>

<style scoped>
</style>
