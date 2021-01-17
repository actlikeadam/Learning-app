<template>
<!-- we have only 1 header, that's why 'The' -->
  <header>
    <h1>{{ title }}</h1>
  </header>
</template>

<script>
export default {
  // App.vue/the parent is passing 'title' here
  props: ['title']
}
</script>

<style scoped>
header {
  width: 100%;
  height: 5rem;
  background-color: #640032;
  display: flex;
  justify-content: center;
  align-items: center;
}

header h1 {
  color: white;
  margin: 0;
}
</style>