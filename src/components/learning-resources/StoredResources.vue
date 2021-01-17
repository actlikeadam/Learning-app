<template>
   <ul>
    <!-- I could use v-for, but have different component for everything and keep this page tiny is the best pattern with JS frameworks -->
      <!-- as we normally pass props TO a component -->
    <learning-resource
      v-for="res in resources"
      :key="res.id"
      :id="res.id"
      :title="res.title"
      :description="res.description"
      :link="res.link">
    </learning-resource>
  </ul>
</template>

<script>
// it's in the same folder
import LearningResource from './LearningResource.vue';

export default {
  inject: ['resources'],
  components: {
    LearningResource
  }
}
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>