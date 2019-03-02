<template>
  <div id="app">
    <router-view/>
    <footer-view/>
  </div>
</template>

<script>
import FooterView from './components/globals/Footer';

export default {
  name: 'App',
  components: {
    FooterView: FooterView,
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  padding: 30px;
}
a {
  color: #42b983;
  font-weight: 600;
  text-decoration: none;
}
a:hover {
  color: #53c28f;
  text-decoration: underline;
}
</style>
