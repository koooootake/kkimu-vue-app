<template>
  <div class="Product">
    <p>{{title}}</p>
    <p class="lead">{{description}}</p>
  </div>
</template>

<script>
export default {
  name: 'Product',
  data: () => {
    return {
      title: 'おしゃべりや',
      description: 'テキストを入力するとしゃべる'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
</style>
