<script setup>
const route = useRoute();
</script>
<template>
  We are in a blog page
  <p>{{ route.params.slug }}</p>
</template>
