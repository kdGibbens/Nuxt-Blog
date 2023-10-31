<script setup>
const { data, pending, error } = await useFetch(
  'https://api.github.com/users/kdGibbens/repos'
);
</script>

<template>
  <p class="mb-2">Github Projects</p>
  <section v-if="pending">Loading...</section>
  <section v-else-if="error">Something went wrong, please try again.</section>
  <section v-else>
    <ul>
      <a
        v-for="item in data"
        :key="item.id"
        :href="item.html_url"
        target="_blank"
        ><li>{{ item.name }}</li></a
      >
    </ul>
  </section>
</template>
