<template>
  <main id="content">
    <h1>kkimu</h1>
    <section id="About">
      <h2>About</h2>
      <About/>
    </section>
    <section id="Product">
      <h2>Product</h2>
      <Products/>
    </section>
    <section id="Publication">
      <h2>Publication</h2>
      <Publications/>
    </section>
  </main>
</template>

<script>
import About from './About';
import Products from './Products';
import Publications from './Publications';
export default {
  name: 'main',
  components: { About, Products, Publications },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h1, h2, h3 {
  font-weight: normal;
  word-wrap: break-word;
  margin: 0.6em 0;
}
h1 {
  font-size: 4rem;
  margin: 0;
}
h2 {
  font-size: 3rem;
}
h3 {
  font-size: 2rem;
}
</style>

<style scoped>
main {
  max-width: 1200px;
  margin: 0 auto;
}
</style>
