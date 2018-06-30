<template>
  <div class="Product">
    <p>{{title}}</p>
    <div v-if="youtube" class="iframe-content">
      <iframe v-bind:src="youtube" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
    <div v-if="image_src">
      <img :src="image_src">
    </div>
    <p class="lead">{{description}}</p>
  </div>
</template>

<script>
export default {
  name: 'Product',
  props: ['title', 'description', 'youtube', 'niconico', 'imageFile'],
  data () {
    const image_src = this.imageFile ? require(`../assets/${this.imageFile}`) : '';
    return {
      image_src,
    };
  },
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
