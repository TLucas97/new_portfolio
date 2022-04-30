<template>
  <div class="modal-content pt-4 pb-4">
    <h1 class="text-center code-pro">Weather App</h1>
    <hr class="modal-line" />
    <div>
      <img
        src="~/static/img/weather.png"
        class="mobile-project-img mt-4 mb-4"
      />
    </div>
    <div>
      <h2 class="code-pro">Descrição</h2>
      <hr class="mb-2 mt-2" />
      <p class="code-pro">
        - Aplicativo web que fornece dados de clima baseado na sua pesquisa
      </p>
      <h2 class="code-pro mt-7">Tecnologias</h2>
      <hr class="mb-2 mt-2" />
      <v-icon x-large color="yellow">mdi-language-javascript</v-icon>
      <v-icon x-large color="red">mdi-language-html5</v-icon>
      <v-icon x-large color="blue">mdi-language-css3</v-icon>
      <v-icon x-large color="green">mdi-vuejs</v-icon>

      <h2 class="code-pro mt-7">Repositório</h2>
      <hr class="mb-2 mt-2" />
      <a
        target="_blank"
        href="https://github.com/TLucas97/clima-weather-app"
        class="font-weight-bold"
      >
        ( Clique aqui para acessar )
      </a>
    </div>
  </div>
</template>

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
