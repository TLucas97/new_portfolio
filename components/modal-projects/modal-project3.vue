<template>
  <div class="modal-content pt-4 pb-4">
    <h1 class="text-center code-pro">{{ urn_title }}</h1>
    <hr class="modal-line" />
    <div>
      <img src="~/static/img/urna.png" class="mobile-project-img mt-4 mb-4" />
    </div>
    <div>
      <h2 class="code-pro">{{ description_title }}</h2>
      <hr class="mb-2 mt-2" />
      <p class="code-pro">
        {{ description }}
      </p>
      <h2 class="code-pro mt-7">{{ tech_title }}</h2>
      <hr class="mb-2 mt-2" />
      <v-icon x-large color="yellow">mdi-language-javascript</v-icon>
      <v-icon x-large color="red">mdi-language-html5</v-icon>
      <v-icon x-large color="blue">mdi-language-css3</v-icon>

      <h2 class="code-pro mt-7">{{ repo_title }}</h2>
      <hr class="mb-2 mt-2" />
      <a
        target="_blank"
        href="https://github.com/TLucas97/Urna-Customizada"
        class="font-weight-bold"
      >
        {{ repo_msg }}
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    urn_title: String,
    description_title: String,
    description: String,
    tech_title: String,
    use_title: String,
    use_msg: String,
    repo_title: String,
    repo_msg: String,
  },
}
</script>

<style scoped>
.modal-content {
  max-width: 80%;
  margin: 0 auto;
}

.modal-line {
  width: 80px;
  height: 5px;
  margin: 0 auto;
  background: black;
}

.mobile-project-img {
  width: 100%;
  border: 2px solid black;
}
</style>
