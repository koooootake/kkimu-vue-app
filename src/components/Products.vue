<template>
  <div class="Products">
    <Product
      v-for="product in products"
      :title="product.title"
      :description="product.description"
      :youtube="product.youtube"
      :imageFile="product.imageFile"
      :media="product.media"
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
