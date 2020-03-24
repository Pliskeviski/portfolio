<template>
  <div class="page-container">
    <link rel="stylesheet" href="node_modules/@fortawesome/fontawesome-free/css/all.css">
    <Section1></Section1>
    <Section2></Section2>
    <Section3></Section3>
  </div>
</template>

<script>
import Section1 from './sections/Section1.vue'
import Section2 from './sections/Section2.vue'
import Section3 from './sections/Section3.vue'

export default {
  name: "MainPage",
  components: {
    Section1,
    Section2,
    Section3
  },
};
</script>

<style scoped>

.page-container {
  margin: 0 10px;
  overflow: auto;
  scroll-snap-type: y mandatory;
  height: 100vh;
}
</style>
