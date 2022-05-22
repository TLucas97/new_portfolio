<template>
  <div class="pt-10 d-xs-none">
    <h1 id="techs" class="code-pro">{{ tech_title }}</h1>
    <hr class="line" />
    <div class="pt-7">
      <v-row>
        <v-col
          ><h4 class="code-pro pb-4">
            <v-icon x-large>mdi-language-javascript</v-icon> Javascript
          </h4></v-col
        >
        <v-col
          ><h4 class="code-pro pb-4">
            <v-icon x-large>mdi-vuejs</v-icon> Vue.js
          </h4></v-col
        >
        <v-col
          ><h4 class="code-pro pb-4">
            <v-icon x-large>mdi-language-html5</v-icon> HTML5
          </h4></v-col
        >
      </v-row>
      <v-row>
        <v-col
          ><h4 class="code-pro pb-4">
            <v-icon x-large>mdi-nuxt</v-icon> Nuxt.js
          </h4></v-col
        >
        <v-col
          ><h4 class="code-pro pb-4">
            <v-icon x-large>mdi-language-css3</v-icon> CSS3
          </h4></v-col
        >
        <v-col
          ><h4 class="code-pro pb-4">
            <v-icon x-large>mdi-vuetify</v-icon> Vuetify.js
          </h4></v-col
        >
      </v-row>
      <v-row>
        <v-col
          ><h4 class="code-pro pb-4"><v-icon x-large>mdi-sass</v-icon> Sass</h4></v-col
        >
        <v-col
          ><h4 class="code-pro pb-4">
            <v-icon x-large>mdi-bootstrap</v-icon> Bootstrap
          </h4></v-col
        >
        <v-col
          ><h4 class="code-pro pb-4"><v-icon x-large>mdi-git</v-icon> Git</h4></v-col
        >
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    tech_title: String,
  }
}
</script>
