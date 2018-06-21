<template>
  <div class="Top">
    <h1>{{ title }}</h1>
    <h2>About</h2>
    <img src="../assets/icon.png" height="150" >
    <h3>Profile</h3>
    <p>木邑 和馬 / Kazuma Kimura</p>
    <p>株式会社サイバーエージェントで働くサーバサイドエンジニア</p>
    <h3>Social</h3>
    <ul>
      <li>
        <a href="https://twitter.com/_kkimu" target="_blank">Twitter</a>
      </li>
      <li>
        <a href="https://github.com/kkimu" target="_blank">Github</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Top',
  data: () => {
    return {
      title: 'kkimu',
      description: 'kkimuaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa',
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
</style>
