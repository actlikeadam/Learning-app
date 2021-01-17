<template>
<!-- title as a normal attr, I wanna pass that text, not a Vue data -->
<the-header title="RememberMe"></the-header>
<!-- :resources is just the same props we have in StoredResources.vue  -->
 <!-- <stored-resources :resources="storedResources"></stored-resources> -->
<the-resources></the-resources>
</template>

<script>
// import StoredResources from './components/learning-resources/StoredResources.vue';
import TheHeader from './components/layouts/TheHeader.vue';
import TheResources from './components/learning-resources/TheResources.vue';

export default {
  components: {
    // StoredResources,
    TheHeader,
    TheResources
  },
  // data() {
  //   return {
  //     // our resources stored as an array of objects
  //     storedResources: [
  //       {
  //         id: 'official-guide',
  //         title: 'Official Guide',
  //         description: 'The official Vue.js documentation.',
  //         link: 'https://vuejs.org',
  //       },
  //       {
  //         id: 'google',
  //         title: 'Google',
  //         description: 'Learn to google...',
  //         link: 'https://google.com',
  //       },
  //     ],
  //   };
  // },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>