<template>
  <div class="product">
    <figure class="product-figure">
      <div v-if="youtube" class="iframe-content">
        <iframe :src="youtube" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
      </div>
      <div v-if="image_src" class="image-content">
        <img :src="image_src">
      </div>
    </figure>
    <div class="product-body">
      <h1>{{title}}</h1>
      <p class="lead">{{description}}</p>
      <p class="media">
        <span v-for="(medium, i) in media">
          <a :href="medium.link" target="_blank">{{medium.text}}</a>
          <span v-if="medium.description">{{medium.description}}</span>
          <span v-if="i !== media.length - 1"> / </span>
        </span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Product',
  props: ['title', 'description', 'youtube', 'imageFile', 'media'],
  data () {
    const image_src = this.imageFile ? require(`../assets/${this.imageFile}`) : '';
    return {
      image_src,
    };
  },
};
</script>

<style scoped>
.product {
  margin: 0 3em 2em 0;
  width: 350px;
  max-width: 100%;
  background: #fff;
}
figure {
  margin: 0;
}
.product-body {
  padding: 0.7em 0.5em;
}
h1 {
  font-size: 18px;
  font-weight: 700;
  margin: 0;
}
p {
  margin: 0.5em 0 0;
}
.iframe-content {
  position: relative;

  width: 350px;
  max-width: 100%;
  height: 250px;
}
.iframe-content iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
.image-content {
  width: 350px;
  max-width: 100%;
}
.image-content img {
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

</style>
