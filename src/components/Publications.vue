<template>
  <ol class="Publications">

    <Publication
      v-for="publication in publications"
      v-bind:text="publication.text"
      v-bind:url="publication.url"
      :key="publication.text"
    />
  </ol>
</template>

<script>
import Publication from "./Publication";

export default {
  name: 'Publications',
  components: {Publication},
  data: () => {
    return {
      publications: require("../data/publications.json")
    }
  }
}
</script>

<style scoped>
</style>
