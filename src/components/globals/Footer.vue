<template>
  <footer>
    <p>{{copyright}}</p>
  </footer>
</template>

<script>
export default {
  data(){
    return{
      copyright: '© 2019 kkimu',
    };
  },
};
</script>

<style>
footer {
  max-width: 1200px;
  margin: 0 auto;
  padding-top: 70px;
}
</style>
