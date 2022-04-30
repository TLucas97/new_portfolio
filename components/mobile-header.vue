<template>
  <div id="header">
    <div id="home"></div>
    <v-card class="mx-auto overflow-hidden" height="2850">
      <v-app-bar color="white" class="app-bar-fixed">
        <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
        <v-toolbar-title>
          <div class="d-flex justify-space-between align-center">
            <div>
              <h6 class="code-pro">TARCISIO ALMEIDA</h6>
            </div>
            <div class="d-flex align-center ml-14">
              <small class="mr-2">PT-BR</small>
              <img
                src="https://cdn-icons-png.flaticon.com/512/197/197386.png"
                width="25"
              />
            </div>
          </div>
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
          <v-btn
            dark
            width="210"
            height="55"
            class="mb-5 text-h5 d-flex justify-space-between"
          >
            <span>LINKEDIN</span>
            <v-icon>mdi-linkedin</v-icon>
          </v-btn>
          <v-btn
            dark
            width="210"
            height="55"
            class="mb-5 text-h5 d-flex justify-space-between"
          >
            <span>GITHUB</span>
            <v-icon>mdi-github</v-icon>
          </v-btn>
          <v-btn
            dark
            width="210"
            height="55"
            class="mb-5 text-h5 d-flex justify-space-between"
          >
            <span>CONTATO</span>
            <v-icon>mdi-account-box</v-icon>
          </v-btn>
          <v-btn
            dark
            width="210"
            height="55"
            class="mb-5 text-h5 d-flex justify-space-between"
          >
            <span>CURRÍCULO</span>
            <v-icon>mdi-file-account</v-icon>
          </v-btn>
        </div>
      </div>
      <div class="pt-16 profile-content">
        <div>
          <h1 id="about-me" class="code-pro">Sobre mim</h1>
          <hr class="line" />
          <div class="pt-5">
            <p class="code-pro text-justify">
              <strong>• Experiência profissional</strong> <br />
              -
              <span
                >Atualmente trabalho como Desenvolvedor Front-end na
                <a target="_blank" href="https://www.suthub.com/"
                  ><span class="suthub-text">SUTHUB</span></a
                >, atuando na criação de aplicações web e fornecendo suporte em
                projetos contínuos.</span
              >
            </p>
            <p class="code-pro text-justify">
              <strong>• Meu objetivo</strong><br />
              -
              <span
                >Como desenvolvedor, fui capaz de perceber a satisfação de
                causar impacto na resolução de problemas, atuar nesse tipo de
                ambiente nos permite entender a importância de alcançar
                objetivos e reconhecer os mesmos com clareza. Foi através dessa
                percepção que decidi tornar como objetivo de vida resolver
                problemas de forma cada vez mais eficiente.</span
              >
            </p>
            <p class="code-pro text-justify">
              <strong>• O início</strong>
              -
              <span
                >Em 2021 dei início a minha jornada para a carreira na área de
                desenvolvimento, desde então tenho trabalhado na criação de
                aplicações para fins de estudo e no início de 2022 tive a
                oportunidade de trabalhar em projetos reais. Isso me
                possibilitou alavancar meus estudos e me motivar a cada vez mais
                buscar conhecimento e explorar as possibilidades que cada
                tecnologia me permitia obter.</span
              >
            </p>
          </div>
        </div>
        <div class="pt-10">
          <h1 id="techs" class="code-pro">Tecnologias</h1>
          <hr class="line" />
          <div class="pt-7">
            <v-row>
              <v-col><h4 class="code-pro pb-4"><v-icon>mdi-language-javascript</v-icon> Javascript</h4></v-col>
              <v-col><h4 class="code-pro pb-4"><v-icon>mdi-vuejs</v-icon> Vue.js</h4></v-col>
            </v-row>
            <v-row>
              <v-col><h4 class="code-pro pb-4"><v-icon>mdi-language-html5</v-icon> HTML5</h4></v-col>
              <v-col><h4 class="code-pro pb-4"><v-icon>mdi-nuxt</v-icon> Nuxt.js</h4></v-col>
            </v-row>
            <v-row>
              <v-col><h4 class="code-pro pb-4"><v-icon>mdi-language-css3</v-icon> CSS3</h4></v-col>
              <v-col><h4 class="code-pro pb-4"><v-icon>mdi-vuetify</v-icon> Vuetify.js</h4></v-col>
            </v-row>
            <v-row>
              <v-col><h4 class="code-pro pb-4"><v-icon>mdi-sass</v-icon> Sass</h4></v-col>
              <v-col><h4 class="code-pro pb-4"><v-icon>mdi-bootstrap</v-icon> Bootstrap</h4></v-col>
            </v-row>
          </div>
        </div>
        <div class="pt-10">
          <h1 class="code-pro">Outros</h1>
          <hr class="line" />
          <div class="pt-7">
            <v-row>
              <v-col><h4 class="code-pro pb-4"><v-icon>mdi-git</v-icon> Git</h4></v-col>
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
              v-model="currentIndex"
              :continuous="false"
              :show-arrows="false"
              hide-delimiter-background
              height="230"
            >
              <v-carousel-item v-for="(slide, i) in slides" :key="i">
                <v-sheet :color="colors[i]" height="100%" tile>
                  <v-row class="fill-height" align="center" justify="center">
                    <div class="white--text text-center">
                      <h1>{{ slide }}</h1>
                      <v-icon color="yellow" class="pb-2"
                        >mdi-lightbulb-on</v-icon
                      >
                      <br />
                      <small class="grey--text"
                        >Clique para mais detalhes</small
                      >
                    </div>
                  </v-row>
                </v-sheet>
              </v-carousel-item>
            </v-carousel>
            <v-list>
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
    currentIndex: 0,
    drawer: false,
    group: null,
    colors: ['secondary', 'secondary', 'secondary', 'secondary', 'secondary'],
    slides: [
      'Covid-Tracker',
      'HarryPotter-Wiki',
      'Urna eletrônica',
      'Brawstars-Data',
      'Weather-app',
    ],
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

.suthub-text {
  font-weight: bold;
  color: #009187;
}
</style>
