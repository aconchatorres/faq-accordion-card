<template>
  <div id="app">
    <FAQ/>
  </div>
</template>

<script>
import FAQ from './components/views/FAQ.vue'

export default {
  name: 'App',
  components: {
    FAQ
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@400;700&display=swap');

html {
  overflow-y: auto !important;
}
#app {
  font-family: 'Kumbh Sans', sans-serif;
  color: hsl(238, 29%, 16%);
}
</style>
