<template>
  <div class="Top">
    <h1>{{ title }}</h1>
    <h2>About</h2>
    <img src="../assets/icon.png" height="150" >
    <h3>Profile</h3>
    <p>{{name}}</p>
    <p>{{description}}</p>
    <h3>Social</h3>
    <ul>
      <li>
        <i class="fab fa-twitter fa-gray"></i>
        <a href="https://twitter.com/_kkimu" target="_blank">@_kkimu</a>
      </li>
      <li>
        <i class="fab fa-github fa-gray"></i>
        <a href="https://github.com/kkimu" target="_blank">id: kkimu</a>
      </li>
    </ul>
    <h2>Products</h2>
    <Products/>
  </div>
</template>

<script>
import Products from "./Products";
export default {
  name: 'Top',
  components: {Products},
  data: () => {
    return {
      title: 'kkimu',
      name: '木邑 和馬 / Kazuma Kimura',
      description: '株式会社サイバーエージェントで働くサーバサイドエンジニア',
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2, h3 {
  font-weight: normal;
  word-wrap: break-word;
}
h1 {
  font-size: 4rem;
}
h2 {
  font-size: 3rem;
}
h3 {
  font-size: 2rem;
}
img {
  height:
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
  line-height: 2;
}
a {
  color: #42b983;
}
.fab {
  margin: 0 5px;
  font-size: 18px;
}
.fa-gray:before
{
  color: #808080 ;
}
</style>
