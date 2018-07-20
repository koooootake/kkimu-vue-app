<template>
  <li class="Publication">
    <span class="lead" v-html="text"></span>
    <a :href="url" target="_blank" v-if="url">link</a>
  </li>
</template>

<script>
export default {
  name: 'Publication',
  props: ['text', 'url'],
};
</script>
<style>
.Publication {
  margin-top: 10px;
}
span.author {
  font-weight: bold;
  text-decoration: underline;
}
</style>

