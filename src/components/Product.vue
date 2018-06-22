<template>
  <div class="Product">
    <p>{{title}}</p>
    <p class="lead">{{description}}</p>
  </div>
</template>

<script>
export default {
  name: 'Product',
  props: ['title', 'description'],
}
</script>

<style scoped>
p {
  font-family: 'Ruda', sans-serif;
  font-size: 16px;
  font-weight: 700;
  margin-top: 15px;
}
p.lead {
  font-family: 'Ruda', sans-serif;
  font-size: 14px;
  font-weight: 400;
  margin-top: -15px;
}
</style>
