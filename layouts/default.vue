<template>
  <v-app>
    <mobile-layolt class="d-md-none" />
    <desktop-layolt class="d-sm-none d-md-block" />
    <Nuxt />
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Source+Code+Pro&display=swap');
.code-pro {
  font-family: 'Source Code Pro', monospace;
}

.line {
  background: black;
  height: 5px;
  width: 250px;
}

a {
  text-decoration: none;
  color: black;
}

html {
  scroll-behavior: smooth;
}
</style>
