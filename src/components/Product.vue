<template>
  <div class="Product">
    <p>{{title}}</p>
    <div v-if="youtube" class="iframe-content">
      <iframe v-bind:src="youtube" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
    <p class="lead">{{description}}</p>
  </div>
</template>

<script>
export default {
  name: 'Product',
  props: ['title', 'description', 'youtube', 'niconico'],
};
</script>

<style scoped>
.Product {
  padding-bottom: 10px;
}
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
.iframe-content {
  position: relative;
  width: 100%;
  height: 0;
  padding-top: 75%;
}
.iframe-content iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
