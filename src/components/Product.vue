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
      <p>{{title}}</p>
      <p class="lead">{{description}}</p>
      <span class="media" v-for="(medium, i) in media">
        <a :href="medium.link" target="_blank">{{medium.text}}</a>
        <span v-if="medium.description">{{medium.description}}</span>
        <span v-if="i !== media.length - 1"> / </span>
      </span>
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
  margin: 1em 3em 1em 0;
  width: 350px;
  background: #fff;
}

figure {
  margin: 0;
}
p {
  font-size: 16px;
  font-weight: 700;
  margin-top: 15px;
}
.lead {
  font-size: 14px;
  font-weight: 400;
}
.iframe-content {
  position: relative;

  width: 350px;
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
}
.image-content img {
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
.product-body {
  padding: 0.5em;
}
.media {
  font-size: 14px;
  font-weight: 600;
}
</style>
