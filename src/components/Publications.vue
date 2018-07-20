<template>
  <ol class="Publications">

    <Publication
      v-for="publication in publications"
      :text="publication.text"
      :url="publication.url"
      :key="publication.text"
    />
  </ol>
</template>

<script>
import Publication from './Publication';

export default {
  name: 'Publications',
  components: { Publication },
  data: () => {
    return {
      publications: require('../data/publications.json'),
    };
  },
};
</script>

<style scoped>
ol {
  padding-inline-start: 20px;
  margin-bottom: 0;
}
</style>
