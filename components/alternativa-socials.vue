<template>
  <div class="pt-12 forced-layolt">
    <v-row>
      <v-col>
        <a
          target="_blank"
          href="https://www.linkedin.com/in/tarcisio-almeida-0a5577207/"
        >
          <v-btn
            dark
            width="210"
            height="55"
            class="mb-5 text-h5 d-flex justify-space-between"
          >
            <span>LINKEDIN</span>
            <v-icon>mdi-linkedin</v-icon>
          </v-btn>
        </a>
      </v-col>
      <v-col>
        <a target="_blank" href="https://github.com/TLucas97">
          <v-btn
            dark
            width="210"
            height="55"
            class="mb-5 text-h5 d-flex justify-space-between"
          >
            <span>GITHUB</span>
            <v-icon>mdi-github</v-icon>
          </v-btn>
        </a>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <a href="#">
          <v-btn
            dark
            width="210"
            height="55"
            class="mb-5 text-h5 d-flex justify-space-between"
          >
            <span>CONTATO</span>
            <v-icon>mdi-account-box</v-icon>
          </v-btn>
        </a>
      </v-col>
      <v-col>
        <v-btn
          dark
          width="210"
          height="55"
          class="mb-5 text-h5 d-flex justify-space-between"
        >
          <span>CURRÍCULO</span>
          <v-icon>mdi-file-account</v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </div>
</template>

<style scoped>
@media (max-width: 800px) {
  .forced-layolt {
    display: none !important;
  }
}
</style>
