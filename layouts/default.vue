<template>
  <v-app>
    <mobile-header />
    <Nuxt />
    <mobile-footer />
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

.line{
  background: black;
  height: 5px;
  width: 250px
}

a{
  text-decoration: none;
  color: black;
}
</style>
