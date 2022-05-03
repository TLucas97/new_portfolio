<template>
  <div id="header">
    <div id="home"></div>
    <v-card class="mx-auto overflow-hidden">
      <v-app-bar color="white" class="app-bar-fixed">
        <div
          class="d-flex align-center justify-space-between"
          style="width: 100%"
        >
          <div class="d-flex align-center">
            <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
            <h3 class="code-pro">TARCISIO ALMEIDA</h3>
          </div>
          <div class="d-flex align-center">
            <!-- COUNTRY SELECTION -->
            <v-menu offset-y close-on-click>
              <template #activator="{ on }">
                <v-btn class="black--text" elevation="0" text v-on="on">
                  <span class="pr-2">PT-BR</span>
                  <img
                    src="https://cdn-icons.flaticon.com/png/512/4087/premium/4087479.png?token=exp=1651538089~hmac=04ae174cdf399778957c05135bc5b44c"
                    alt=""
                    width="30"
                  />
                  <v-icon right> mdi-chevron-down </v-icon>
                </v-btn>
              </template>

              <v-list>
                <v-list-item-group v-model="countriesLang.id">
                  <v-list-item
                    v-for="(titles, idx) in countriesLang"
                    :key="idx"
                    value="titles"
                  >
                    <v-btn
                      text
                      class="black--text d-flex justify-space-between align-center"
                    >
                      <span class="pr-2 black--text font-weight-bold">{{
                        titles.name
                      }}</span>
                      <div>
                        <img :src="titles.pic" width="30" />
                      </div>
                    </v-btn>
                  </v-list-item>
                </v-list-item-group>
              </v-list>
            </v-menu>
            <!-- COUNTRY SELECTION -->
          </div>
        </div>
      </v-app-bar>
      <!-- content -->
      <div class="inside-content pt-16">
        <div class="pt-10">
          <img
            src="~/static/img/tarcisio2.png"
            width="200"
            class="profile-img"
          />
        </div>
        <div class="pt-12 d-flex flex-column">
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
              <span
                >- Atualmente trabalho como Desenvolvedor Front-end na
                <a target="_blank" href="https://www.suthub.com/"
                  ><span class="suthub-text">SUTHUB</span></a
                >, atuando na criação de aplicações web e fornecendo suporte em
                projetos contínuos.</span
              >
            </p>
            <p class="code-pro text-justify">
              <strong>• Meu objetivo</strong><br />
              <span
                >- Como desenvolvedor, fui capaz de perceber a satisfação de
                causar impacto na resolução de problemas, atuar nesse tipo de
                ambiente nos permite entender a importância de alcançar
                objetivos e reconhecer os mesmos com clareza. Foi através dessa
                percepção que decidi tornar como objetivo de vida resolver
                problemas de forma cada vez mais eficiente.</span
              >
            </p>
            <p class="code-pro text-justify">
              <strong>• O início</strong> <br />
              <span
                >- Em 2021 dei início a minha jornada para a carreira na área de
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
              <v-col
                ><h4 class="code-pro pb-4">
                  <v-icon>mdi-language-javascript</v-icon> Javascript
                </h4></v-col
              >
              <v-col
                ><h4 class="code-pro pb-4">
                  <v-icon>mdi-vuejs</v-icon> Vue.js
                </h4></v-col
              >
            </v-row>
            <v-row>
              <v-col
                ><h4 class="code-pro pb-4">
                  <v-icon>mdi-language-html5</v-icon> HTML5
                </h4></v-col
              >
              <v-col
                ><h4 class="code-pro pb-4">
                  <v-icon>mdi-nuxt</v-icon> Nuxt.js
                </h4></v-col
              >
            </v-row>
            <v-row>
              <v-col
                ><h4 class="code-pro pb-4">
                  <v-icon>mdi-language-css3</v-icon> CSS3
                </h4></v-col
              >
              <v-col
                ><h4 class="code-pro pb-4">
                  <v-icon>mdi-vuetify</v-icon> Vuetify.js
                </h4></v-col
              >
            </v-row>
            <v-row>
              <v-col
                ><h4 class="code-pro pb-4">
                  <v-icon>mdi-sass</v-icon> Sass
                </h4></v-col
              >
              <v-col
                ><h4 class="code-pro pb-4">
                  <v-icon>mdi-bootstrap</v-icon> Bootstrap
                </h4></v-col
              >
            </v-row>
            <v-row>
              <v-col
                ><h4 class="code-pro pb-4">
                  <v-icon>mdi-git</v-icon> Git
                </h4></v-col
              >
            </v-row>
          </div>
        </div>
        <div class="pt-10">
          <h1 class="code-pro">Outros</h1>
          <hr class="line" />
          <div class="pt-7">
            <v-row>
              <v-col><h4 class="code-pro pb-4">➤ SCRUM</h4></v-col>
              <v-col><h4 class="code-pro pb-4">➤ Adobe XD</h4></v-col>
            </v-row>
            <v-row>
              <v-col><h4 class="code-pro pb-4">➤ Figma</h4></v-col>
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
              :continuous="true"
              :show-arrows="true"
              height="auto"
            >
              <v-carousel-item
                v-for="(slide, i) in slides"
                :key="i"
                @click="openDialog"
              >
                <v-sheet :color="colors[i]" height="auto" tile>
                  <v-row class="fill-height" align="center" justify="center">
                    <div
                      class="white--text text-center d-flex align-center justify-center flex-column"
                      style="height: 250px"
                    >
                      <h1>{{ slide }}</h1>
                      <v-icon color="yellow" class="pb-2"
                        >mdi-lightbulb-on</v-icon
                      >
                      <br />
                      <small class="white--text"
                        >Clique para mais detalhes</small
                      >
                    </div>
                  </v-row>
                </v-sheet>
              </v-carousel-item>
            </v-carousel>
            <v-list height="95">
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
      <!-- Modal projects -->
      <div>
        <v-row justify="center">
          <v-dialog
            v-model="dialog"
            fullscreen
            hide-overlay
            transition="dialog-bottom-transition"
          >
            <v-card>
              <v-toolbar color="white">
                <v-btn icon dark @click="dialog = false">
                  <v-icon color="black">mdi-close</v-icon>
                </v-btn>
                <v-toolbar-title class="text--center code-pro"
                  >Projetos</v-toolbar-title
                >
              </v-toolbar>
              <modal-project1 v-show="modals.modal_1" />
              <modal-project2 v-show="modals.modal_2" />
              <modal-project3 v-show="modals.modal_3" />
              <modal-project4 v-show="modals.modal_4" />
              <modal-project5 v-show="modals.modal_5" />
            </v-card>
          </v-dialog>
        </v-row>
      </div>
      <!-- Modal projects -->
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    currentIndex: 0,
    countriesLang: [
      {
        id: 1,
        name: 'EN-US',
        pic: 'https://cdn-icons-png.flaticon.com/512/206/206626.png',
      },
    ],
    dialog: false,
    modals: {
      modal_1: false,
      modal_2: false,
      modal_3: false,
      modal_4: false,
      modal_5: false,
    },
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
  methods: {
    openDialog() {
      if (this.currentIndex === 0) {
        this.dialog = true
        this.modals.modal_1 = true
        this.modals.modal_2 = false
        this.modals.modal_3 = false
        this.modals.modal_4 = false
        this.modals.modal_5 = false
      } else if (this.currentIndex === 1) {
        this.dialog = true
        this.modals.modal_1 = false
        this.modals.modal_2 = true
        this.modals.modal_3 = false
        this.modals.modal_4 = false
        this.modals.modal_5 = false
      } else if (this.currentIndex === 2) {
        this.dialog = true
        this.modals.modal_1 = false
        this.modals.modal_2 = false
        this.modals.modal_3 = true
        this.modals.modal_4 = false
        this.modals.modal_5 = false
      } else if (this.currentIndex === 3) {
        this.dialog = true
        this.modals.modal_1 = false
        this.modals.modal_2 = false
        this.modals.modal_3 = false
        this.modals.modal_4 = true
        this.modals.modal_5 = false
      } else if (this.currentIndex === 4) {
        this.dialog = true
        this.modals.modal_1 = false
        this.modals.modal_2 = false
        this.modals.modal_3 = false
        this.modals.modal_4 = false
        this.modals.modal_5 = true
      }
    },
  },
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
