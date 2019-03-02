<template>
  <div class="About">
    <img src="../assets/icon.png" height="150" alt="kkimu">
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
  </div>
</template>

<script>
export default {
  name: 'About',
  data: () => {
    return {
      name: '木邑 和馬 / Kazuma Kimura',
      description: '株式会社サイバーエージェント/マッチングエージェントで働くバックエンドエンジニア。ものづくりとビジネスが好き。',
    };
  },
};
</script>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
  line-height: 2;
}
.fab {
  margin-right: 5px;
  font-size: 1.1rem;
}
.fa-gray:before {
  color: #808080 ;
}
</style>
