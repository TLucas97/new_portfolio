<template>
  <div id="header">
    <div id="home"></div>
    <v-card class="mx-auto overflow-hidden" height="2650">
      <v-app-bar color="white" class="app-bar-fixed">
        <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
        <v-toolbar-title>
          <h4 class="code-pro">TARCISIO ALMEIDA</h4>
        </v-toolbar-title>
      </v-app-bar>
      <!-- content -->
      <div class="inside-content pt-16">
        <div class="pt-10">
          <img
            src="~/static/img/tarcisio.png"
            width="200"
            class="profile-img"
          />
        </div>
        <div class="pt-12 d-flex flex-column">
          <v-btn dark class="mb-5 text-h5">LINKEDIN</v-btn>
          <v-btn dark class="mb-5 text-h5">GITHUB</v-btn>
          <v-btn dark class="mb-5 text-h5">CONTATO</v-btn>
          <v-btn dark class="mb-5 text-h5">CURRÍCULO</v-btn>
        </div>
      </div>
      <div class="pt-16 profile-content">
        <div>
          <h1 id="about-me" class="code-pro">Sobre mim</h1>
          <hr class="line" />
          <div class="pt-5">
            <p class="code-pro text-justify">
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Repudiandae, quas sed. Asperiores ea nam doloribus explicabo,
              ducimus consectetur atque id quisquam eos. Officiis, voluptas
              neque? Quos tempora itaque ullam repellendus beatae. Nostrum iste
              illum quis vitae voluptas ipsa nisi sunt natus commodi fuga.
              Recusandae iusto minus dolores ab eaque necessitatibus at, officia
              iure error in vitae doloremque eveniet voluptatibus unde nihil
              quibusdam pariatur voluptate culpa mollitia totam. Tenetur qui,
              temporibus deleniti laboriosam laborum eius facilis. Asperiores
              doloribus libero saepe quasi assumenda! Iure fuga, optio,
              doloremque reiciendis aut eum nesciunt natus ut pariatur odio modi
              est blanditiis dicta nobis velit mollitia.
            </p>
          </div>
        </div>
        <div class="pt-10">
          <h1 id="techs" class="code-pro">Tecnologias</h1>
          <hr class="line" />
          <div class="pt-7">
            <v-row>
              <v-col><h4 class="code-pro pb-4">➤ Javascript</h4></v-col>
              <v-col><h4 class="code-pro pb-4">➤ Vue.js</h4></v-col>
            </v-row>
            <v-row>
              <v-col><h4 class="code-pro pb-4">➤ HTML5</h4></v-col>
              <v-col><h4 class="code-pro pb-4">➤ Nuxt.js</h4></v-col>
            </v-row>
            <v-row>
              <v-col><h4 class="code-pro pb-4">➤ CSS3</h4></v-col>
              <v-col><h4 class="code-pro pb-4">➤ Vuetify.js</h4></v-col>
            </v-row>
            <v-row>
              <v-col><h4 class="code-pro pb-4">➤ Sass</h4></v-col>
              <v-col><h4 class="code-pro pb-4">➤ Bootstrap</h4></v-col>
            </v-row>
          </div>
        </div>
        <div class="pt-10">
          <h1 class="code-pro">Outros</h1>
          <hr class="line" />
          <div class="pt-7">
            <v-row>
              <v-col><h4 class="code-pro pb-4">➤ Git</h4></v-col>
              <v-col><h4 class="code-pro pb-4">➤ Figma</h4></v-col>
            </v-row>
            <v-row>
              <v-col><h4 class="code-pro pb-4">➤ SCRUM</h4></v-col>
              <v-col><h4 class="code-pro pb-4">➤ Adobe XD</h4></v-col>
            </v-row>
          </div>
        </div>
        <div class="pt-10">
          <h1 id="projects" class="code-pro">Projetos</h1>
          <hr class="line" />
          <v-card elevation="24" max-width="444" class="mx-auto mt-7">
            <v-system-bar lights-out></v-system-bar>
            <v-carousel
              :continuous="false"
              :show-arrows="false"
              hide-delimiter-background
              height="300"
            >
              <v-carousel-item v-for="(slide, i) in slides" :key="i">
                <v-sheet :color="colors[i]" height="100%" tile>
                  <v-row class="fill-height" align="center" justify="center">
                    <div class="text-h2">{{ slide }}</div>
                  </v-row>
                </v-sheet>
              </v-carousel-item>
            </v-carousel>
            <v-list two-line>
              <v-list-item>
                <v-list-item-avatar>
                  <img src="~/static/img/tarcisio.png" alt="" />
                </v-list-item-avatar>
                <v-list-item-content>
                  <v-list-item-title>Tarcísio Almeida</v-list-item-title>
                  <v-list-item-title class="font-weight-bold"
                    >• Projetos</v-list-item-title
                  >
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-card>
        </div>
      </div>
      <!-- content -->
      <v-navigation-drawer
        v-model="drawer"
        absolute
        temporary
        class="app-bar-fixed"
      >
        <v-list>
          <v-list-item-group v-model="group">
            <a href="#home">
              <v-list-item>
                <v-list-item-icon>
                  <v-icon>mdi-home</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Home</v-list-item-title>
              </v-list-item>
            </a>
            <a href="#about-me">
              <v-list-item>
                <v-list-item-icon>
                  <v-icon>mdi-account-alert</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Sobre mim</v-list-item-title>
              </v-list-item>
            </a>
            <a href="#techs">
              <v-list-item>
                <v-list-item-icon>
                  <v-icon>mdi-language-javascript</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Tecnologias</v-list-item-title>
              </v-list-item>
            </a>
            <a href="#projects">
              <v-list-item>
                <v-list-item-icon>
                  <v-icon>mdi-lightbulb-on</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Projetos</v-list-item-title>
              </v-list-item>
            </a>
        </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
    colors: [
      'green',
      'secondary',
      'yellow darken-4',
      'red lighten-2',
      'orange darken-1',
    ],
    slides: ['First', 'Second', 'Third', 'Fourth', 'Fifth'],
  }),
}
</script>

<style scoped>
.inside-content {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.profile-img {
  border-radius: 15px;
  -webkit-box-shadow: 0px 9px 0px 6px rgba(0, 0, 0, 0.1),
    0px 12px 0px 8px rgba(0, 0, 0, 0.1), 0px 15px 0px 10px rgba(0, 0, 0, 0.1),
    0px 18px 0px 12px rgba(0, 0, 0, 0.1), 50px -50px 50px 50px rgba(0, 0, 0, 0);
  box-shadow: 0px 9px 0px 6px rgba(0, 0, 0, 0.1),
    0px 12px 0px 8px rgba(0, 0, 0, 0.1), 0px 15px 0px 10px rgba(0, 0, 0, 0.1),
    0px 18px 0px 12px rgba(0, 0, 0, 0.1), 50px -50px 50px 50px rgba(0, 0, 0, 0);
}

.profile-content {
  max-width: 80%;
  margin: 0 auto;
}

.app-bar-fixed {
  position: fixed;
  z-index: 1;
}
</style>
