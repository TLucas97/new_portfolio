<template>
  <div class="desktop code-pro" :class="dark_mode">
    <div class="change-lang-btn">
      <v-menu offset-y close-on-click top>
        <template #activator="{ on }">
          <v-btn elevation="0" text v-on="on">
            <span class="pr-2" :class="dark_mode">{{ translate('currentName') }}</span>
            <img :src="translate('currentFlag')" alt="" width="20" />
            <v-icon :class="dark_mode" right> mdi-chevron-up </v-icon>
          </v-btn>
        </template>

        <v-list style="cursor: pointer">
          <v-list-item-group>
            <small
              style="width: 100%"
              class="font-weight-bold d-flex align-center justify-space-around"
              @click="changeLang"
              >{{ translate('langChange') }}
              <img :src="translate('otherFlag')" width="20" />
            </small>
          </v-list-item-group>
        </v-list>
      </v-menu>
    </div>
    <span id="desktop_home"></span>
    <div
      :class="dark_mode"
      class="desktop-header d-flex justify-space-between align-center"
    >
      <div>
        <h3>Tarcísio Almeida ♡</h3>
      </div>
      <div class="pr-16 mr-8">
        <a href="#desktop_home">
          <v-btn
            :class="dark_mode"
            class="hover-underline-animation font-weight-bold"
            elevation="0"
            >Home</v-btn
          >
        </a>
        <a href="#desktop_tech">
          <v-btn
            :class="dark_mode"
            class="hover-underline-animation font-weight-bold"
            text
            elevation="0"
            >{{ translate('techTitle') }}</v-btn
          >
        </a>
        <a href="#desktop_projects">
          <v-btn
            :class="dark_mode"
            class="hover-underline-animation font-weight-bold"
            text
            elevation="0"
            >{{ translate('projectsTitle') }}</v-btn
          >
        </a>
      </div>
      <div>
        <v-btn
          :class="dark_mode"
          class="dark-mode-hover"
          text
          @click="darkMode"
        >
          <small>Dark mode</small>
          <v-icon :class="dark_mode" color="yellow" class="pb-2 pl-2"
            >mdi-{{ lightbulb }}</v-icon
          >
        </v-btn>
      </div>
    </div>

    <div class="desktop-wrapper pt-15 pb-5">
      <div class="smooth-white-box">
        <v-row>
          <v-col cols="4"
            ><img
              src="~/static/img/tarcisio2.png"
              style="width: 90%; border-radius: 15px"
            />
            <p class="mt-5">
              <strong>{{ translate('cardNameLabel') }}</strong> Tarcísio Almeida
            </p>
            <p>
              <strong>{{ translate('cardAgeLabel') }}</strong> {{ translate('cardAge') }}
            </p>
            <p>
              <strong>{{ translate('cardProfessionLabel') }}</strong>
              {{ translate('cardProfession') }}
            </p>
            <p>
              <strong>{{ translate('cardNacionalityLabel') }}</strong>
              {{ translate('cardNacionality') }}
            </p>
          </v-col>
          <v-col>
            <h2>{{ translate('aboutTitle') }}</h2>
            <h3 class="mt-5">{{ translate('subTitle1') }}</h3>
            <p style="font-size: 1rem">{{ translate('subText1') }}</p>
            <h3 class="mt-5">{{ translate('subTitle2') }}</h3>
            <p style="font-size: 1rem">{{ translate('subText2') }}</p>
            <h3 class="mt-5">{{ translate('subTitle3') }}</h3>
            <p style="font-size: 1rem">{{ translate('subText3') }}</p>
          </v-col>
        </v-row>
      </div>
      <div
        class="pt-16 d-flex align-center wrap"
        style="justify-content: space-evenly"
      >
        <div>
          <a
            target="_blank"
            href="https://www.linkedin.com/in/tarcisio-almeida-0a5577207/"
          >
            <v-btn
              color="#E1E1E1"
              width="210"
              height="55"
              class="mb-5 text-h5 d-flex justify-space-between"
            >
              <span>LINKEDIN</span>
              <v-icon>mdi-linkedin</v-icon>
            </v-btn>
          </a>
        </div>
        <div>
          <a target="_blank" href="https://github.com/TLucas97">
            <v-btn
              color="#E1E1E1"
              width="210"
              height="55"
              class="mb-5 text-h5 d-flex justify-space-between"
            >
              <span>GITHUB</span>
              <v-icon>mdi-github</v-icon>
            </v-btn>
          </a>
        </div>
        <div>
          <a href="#">
            <v-btn
              color="#E1E1E1"
              width="210"
              height="55"
              class="mb-5 text-h5 d-flex justify-space-between"
            >
              <span>{{ translate('socialsCV') }}</span>
              <v-icon>mdi-file-account</v-icon>
            </v-btn>
          </a>
        </div>
        <div>
          <a target="_blank" href="mailto:tarcisio.almeida197@gmail.com">
            <v-btn
            color="#E1E1E1"
            width="210"
            height="55"
            class="mb-5 text-h5 d-flex justify-space-between"
          >
            <span>{{ translate('socialsContact') }}</span>
            <v-icon>mdi-account-box</v-icon>
          </v-btn>
          </a>
        </div>
      </div>

      <span id="desktop_tech"></span>
      <div class="pt-16 mt-5">
        <h1 class="text-center">{{ translate('techTitle') }}</h1>
        <hr class="line" style="margin: 0 auto" />
        <div class="pt-9" style="max-width: 80%; margin: 0 auto">
          <v-row>
            <v-col class="d-flex align-center justify-center">
              <v-icon class="color-javascript" size="175"
                >mdi-language-javascript</v-icon
              >
            </v-col>
            <v-col class="d-flex align-center justify-center">
              <v-icon class="color-html" size="175">mdi-language-html5</v-icon>
            </v-col>
            <v-col class="d-flex align-center justify-center">
              <v-icon class="color-css3" size="175">mdi-language-css3</v-icon>
            </v-col>
          </v-row>
          <v-row>
            <v-col class="d-flex align-center justify-center">
              <v-icon class="color-vue" size="175">mdi-vuejs</v-icon>
            </v-col>
            <v-col class="d-flex align-center justify-center">
              <v-icon class="color-nuxt" size="175">mdi-nuxt</v-icon>
            </v-col>
            <v-col class="d-flex align-center justify-center">
              <v-icon class="color-vuetify" size="175">mdi-vuetify</v-icon>
            </v-col>
          </v-row>
          <v-row>
            <v-col class="d-flex align-center justify-center">
              <v-icon class="color-sass" size="175">mdi-sass</v-icon>
            </v-col>
            <v-col class="d-flex align-center justify-center">
              <v-icon class="color-bootstrap" size="175">mdi-bootstrap</v-icon>
            </v-col>
            <v-col class="d-flex align-center justify-center">
              <v-icon class="color-git" size="175">mdi-git</v-icon>
            </v-col>
          </v-row>

          <span id="desktop_projects"></span>
          <div class="pt-16">
            <div>
              <h1 class="text-center">{{ translate('projectsTitle') }}</h1>
              <hr class="line" style="margin: 0 auto" />
              <v-row class="pt-10">
                <v-col v-if="project_1" class="smooth-white-box mr-5">
                  <div class="modal-content pt-4 pb-4">
                    <h1 class="text-center code-pro">Covid Tracker</h1>
                    <hr class="modal-line" />
                    <div>
                      <img
                        src="~/static/img/covid-tracker.png"
                        class="mobile-project-img mt-4 mb-4"
                      />
                    </div>
                    <div>
                      <h2 class="code-pro">{{ translate('descriptionLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <p class="code-pro">
                        {{ translate('descriptionTracker') }}
                      </p>
                      <h2 class="code-pro mt-7">{{ translate('techLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <v-icon x-large color="yellow"
                        >mdi-language-javascript</v-icon
                      >
                      <v-icon x-large color="red">mdi-language-html5</v-icon>
                      <v-icon x-large color="blue">mdi-language-css3</v-icon>

                      <h2 class="code-pro mt-7">{{ translate('useLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <a
                        target="_blank"
                        href="https://sleepy-leavitt-24ad59.netlify.app/"
                        class="font-weight-bold"
                      >
                        {{ translate('useMsg') }}
                      </a>
                      <h2 class="code-pro mt-7">{{ translate('repoLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <a
                        target="_blank"
                        href="https://github.com/TLucas97/covid-tracker"
                        class="font-weight-bold"
                      >
                        {{ translate('repoMsg') }}
                      </a>
                    </div>
                  </div>
                  <v-row class="pt-7">
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj1"
                            v-on="on"
                            >Covid Tracker</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj2"
                            v-on="on"
                            >Harry Potter Wiki</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj3"
                            v-on="on"
                            >{{ translate('urnName') }}</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj4"
                            v-on="on"
                            >BrawlStars Data</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj5"
                            v-on="on"
                            >Weather app</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                  </v-row>
                </v-col>
                <v-col v-if="project_2" class="smooth-white-box">
                  <div class="modal-content pt-4 pb-4">
                    <h1 class="text-center code-pro">Harry Potter Wiki</h1>
                    <hr class="modal-line" />
                    <div>
                      <img
                        src="~/static/img/potter-wiki.png"
                        class="mobile-project-img mt-4 mb-4"
                      />
                    </div>
                    <div>
                      <h2 class="code-pro">{{ translate('descriptionLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <p class="code-pro">
                        {{ translate('descriptionPotter') }}
                      </p>
                      <h2 class="code-pro mt-7">{{ translate('techLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <v-icon x-large color="yellow"
                        >mdi-language-javascript</v-icon
                      >
                      <v-icon x-large color="red">mdi-language-html5</v-icon>
                      <v-icon x-large color="blue">mdi-language-css3</v-icon>
                      <v-icon x-large color="green">mdi-vuejs</v-icon>
                      <v-icon x-large color="blue">mdi-vuetify</v-icon>

                      <h2 class="code-pro mt-7">{{ translate('useLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <a
                        target="_blank"
                        href="https://potter-wiki.netlify.app/"
                        class="font-weight-bold"
                      >
                        {{ translate('useMsg') }}
                      </a>

                      <h2 class="code-pro mt-7">{{ translate('repoLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <a
                        target="_blank"
                        href="https://github.com/TLucas97/hp-data-project"
                        class="font-weight-bold"
                      >
                        {{ translate('repoMsg') }}
                      </a>
                    </div>
                  </div>
                  <v-row class="pt-7">
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj1"
                            v-on="on"
                            >Covid Tracker</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj2"
                            v-on="on"
                            >Harry Potter Wiki</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj3"
                            v-on="on"
                            >{{ translate('urnName') }}</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj4"
                            v-on="on"
                            >BrawlStars Data</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj5"
                            v-on="on"
                            >Weather app</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                  </v-row>
                </v-col>
              </v-row>
              <v-row class="pt-10">
                <v-col v-if="project_3" class="smooth-white-box mr-5">
                  <div class="modal-content pt-4 pb-4">
                    <h1 class="text-center code-pro">{{ translate('urnName') }}</h1>
                    <hr class="modal-line" />
                    <div>
                      <img
                        src="~/static/img/urna.png"
                        class="mobile-project-img mt-4 mb-4"
                      />
                    </div>
                    <div>
                      <h2 class="code-pro">{{ translate('descriptionLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <p class="code-pro">
                        {{ translate('descriptionUrn') }}
                      </p>
                      <h2 class="code-pro mt-7">{{ translate('techLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <v-icon x-large color="yellow"
                        >mdi-language-javascript</v-icon
                      >
                      <v-icon x-large color="red">mdi-language-html5</v-icon>
                      <v-icon x-large color="blue">mdi-language-css3</v-icon>

                      <h2 class="code-pro mt-7">{{ translate('repoLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <a
                        target="_blank"
                        href="https://github.com/TLucas97/Urna-Customizada"
                        class="font-weight-bold"
                      >
                        {{ translate('repoMsg') }}
                      </a>
                    </div>
                  </div>
                  <v-row class="pt-7">
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj1"
                            v-on="on"
                            >Covid Tracker</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj2"
                            v-on="on"
                            >Harry Potter Wiki</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj3"
                            v-on="on"
                            >{{ translate('urnName') }}</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj4"
                            v-on="on"
                            >BrawlStars Data</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj5"
                            v-on="on"
                            >Weather app</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                  </v-row>
                </v-col>
                <v-col v-if="project_4" class="smooth-white-box">
                  <div class="modal-content pt-4 pb-4">
                    <h1 class="text-center code-pro">BrawlStars Data</h1>
                    <hr class="modal-line" />
                    <div>
                      <img
                        src="~/static/img/braw.png"
                        class="mobile-project-img mt-4 mb-4"
                      />
                    </div>
                    <div>
                      <h2 class="code-pro">{{ translate('descriptionLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <p class="code-pro">
                        {{ translate('descriptionBrawl') }}
                      </p>
                      <h2 class="code-pro mt-7">{{ translate('techLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <v-icon x-large color="yellow"
                        >mdi-language-javascript</v-icon
                      >
                      <v-icon x-large color="red">mdi-language-html5</v-icon>
                      <v-icon x-large color="blue">mdi-language-css3</v-icon>
                      <v-icon x-large color="green">mdi-vuejs</v-icon>

                      <h2 class="code-pro mt-7">{{ translate('useLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <a
                        target="_blank"
                        href="https://brawlegends-data.netlify.app/"
                        class="font-weight-bold"
                      >
                        {{ translate('useMsg') }}
                      </a>

                      <h2 class="code-pro mt-7">{{ translate('repoLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <a
                        target="_blank"
                        href="https://github.com/TLucas97/brawstars-data-project/"
                        class="font-weight-bold"
                      >
                        {{ translate('repoMsg') }}
                      </a>
                    </div>
                  </div>
                  <v-row class="pt-7">
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj1"
                            v-on="on"
                            >Covid Tracker</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj2"
                            v-on="on"
                            >Harry Potter Wiki</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj3"
                            v-on="on"
                            >{{ translate('urnName') }}</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj4"
                            v-on="on"
                            >BrawlStars Data</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj5"
                            v-on="on"
                            >Weather app</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                  </v-row>
                </v-col>
              </v-row>
              <v-row class="pt-10">
                <v-col v-if="project_5" class="smooth-white-box mr-6">
                  <div class="modal-content pt-4 pb-4">
                    <h1 class="text-center code-pro">Weather App</h1>
                    <hr class="modal-line" />
                    <div class="d-flex justify-center align-center">
                      <img
                        src="~/static/img/weather.png"
                        class="mt-4 mb-4"
                        style="max-width: 60%"
                      />
                    </div>
                    <div>
                      <h2 class="code-pro">{{ translate('descriptionLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <p class="code-pro">
                        {{ translate('descriptionWeather') }}
                      </p>
                      <h2 class="code-pro mt-7">{{ translate('techLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <v-icon x-large color="yellow"
                        >mdi-language-javascript</v-icon
                      >
                      <v-icon x-large color="red">mdi-language-html5</v-icon>
                      <v-icon x-large color="blue">mdi-language-css3</v-icon>
                      <v-icon x-large color="green">mdi-vuejs</v-icon>

                      <h2 class="code-pro mt-7">{{ translate('repoLabel') }}</h2>
                      <hr class="mb-2 mt-2" />
                      <a
                        target="_blank"
                        href="https://github.com/TLucas97/clima-weather-app"
                        class="font-weight-bold"
                      >
                        {{ translate('repoMsg') }}
                      </a>
                    </div>
                  </div>
                  <v-row class="pt-7">
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj1"
                            v-on="on"
                            >Covid Tracker</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj2"
                            v-on="on"
                            >Harry Potter Wiki</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj3"
                            v-on="on"
                            >{{ translate('urnName') }}</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj4"
                            v-on="on"
                            >BrawlStars Data</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                    <v-col class="d-flex justify-center align-center">
                      <v-tooltip bottom>
                        <template #activator="{ on, attrs }">
                          <v-btn
                            v-bind="attrs"
                            color="primary"
                            @click="changeProj5"
                            v-on="on"
                            >Weather app</v-btn
                          >
                        </template>
                        <span>{{ translate('show') }}</span>
                      </v-tooltip>
                    </v-col>
                  </v-row>
                </v-col>
              </v-row>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import en from '../mixins/en.js'
import ptbr from '../mixins/pt-br.js'

export default {
  mixins: [en, ptbr],
  data() {
    return {
      lightbulb: 'lightbulb-on',
      dark_mode: '',
      lang: 'en',
      project_1: true,
      project_2: false,
      project_3: false,
      project_4: false,
      project_5: false,
    }
  },
  methods: {
    changeProj1() {
      this.project_1 = true
      this.project_2 = false
      this.project_3 = false
      this.project_4 = false
      this.project_5 = false
    },
    changeProj2() {
      this.project_1 = false
      this.project_2 = true
      this.project_3 = false
      this.project_4 = false
      this.project_5 = false
    },
    changeProj3() {
      this.project_1 = false
      this.project_2 = false
      this.project_3 = true
      this.project_4 = false
      this.project_5 = false
    },
    changeProj4() {
      this.project_1 = false
      this.project_2 = false
      this.project_3 = false
      this.project_4 = true
      this.project_5 = false
    },
    changeProj5() {
      this.project_1 = false
      this.project_2 = false
      this.project_3 = false
      this.project_4 = false
      this.project_5 = true
    },
    darkMode() {
      if (this.dark_mode === '' && this.lightbulb === 'lightbulb-on') {
        this.dark_mode = 'dark-mode'
        this.lightbulb = 'lightbulb-off'
      } else if (
        this.dark_mode === 'dark-mode' &&
        this.lightbulb === 'lightbulb-off'
      ) {
        this.dark_mode = ''
        this.lightbulb = 'lightbulb-on'
      }
    },
    translate(prop) {
      return this[this.lang][prop]
    },
    changeLang() {
      if (this.lang === 'en') {
        this.lang = 'ptbr'
      } else if (this.lang === 'ptbr') {
        this.lang = 'en'
      }
    },
  },
}
</script>

<style scoped>
.desktop {
  width: 100%;
}

.desktop-header {
  width: 95%;
  margin: 0 auto;
  position: fixed;
  z-index: 1;
  left: 0;
  right: 0;
  background: white;
  border-bottom: 1px solid rgba(128, 128, 128, 0.301);
}

.desktop-wrapper {
  width: 75%;
  margin: 0 auto;
}

p {
  font-size: 0.85rem;
}

span {
  font-family: 'Source Code Pro', monospace !important;
  font-weight: bold;
}

.change-lang-btn {
  position: fixed;
  right: 0;
  bottom: 0;
  padding-right: 1em;
  padding-bottom: 1em;
}

.smooth-white-box {
  width: 70%;
  margin: 0 auto;
  padding: 1.7em;
  background: rgba(128, 128, 128, 0.24);
  border-radius: 25px;
  -webkit-box-shadow: 0px 9px 18px -3px rgba(0, 0, 0, 0.4);
  -moz-box-shadow: 0px 9px 18px -3px rgba(0, 0, 0, 0.4);
  box-shadow: 0px 9px 18px -3px rgba(0, 0, 0, 0.4);
}

@media (max-width: 1280px) {
  .wrap {
    flex-direction: column;
  }
}

/* Animation */
.dark-mode-hover {
  transition: 0.3s;
}

.dark-mode-hover:hover {
  background: rgba(0, 0, 0, 0.685) !important;
  color: white !important;
}

.hover-underline-animation {
  display: inline-block;
  position: relative;
  border-radius: 0 !important;
}

.hover-underline-animation:after {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 3px;
  bottom: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.685);
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.hover-underline-animation:hover:after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

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
  border-radius: 10px;
}

/* COLORS HOVER */
.color-javascript {
  transition: 0.3s;
}

.color-javascript:hover {
  color: #f2bf26;
}

.color-html {
  transition: 0.3s;
}

.color-html:hover {
  color: #e65e1f;
}
.color-css3 {
  transition: 0.3s;
}

.color-css3:hover {
  color: #2449d8;
}

.color-vue {
  transition: 0.3s;
}

.color-vue:hover {
  color: green;
}

.color-nuxt {
  transition: 0.3s;
}

.color-nuxt:hover {
  color: green;
}

.color-vuetify {
  transition: 0.3s;
}

.color-vuetify:hover {
  color: #528fdf;
}

.color-sass {
  transition: 0.3s;
}

.color-sass:hover {
  color: pink;
}

.color-bootstrap {
  transition: 0.3s;
}

.color-bootstrap:hover {
  color: purple;
}

.color-git {
  transition: 0.3s;
}

.color-git:hover {
  color: rgb(255, 94, 0);
}

/* Darkmode */
.dark-mode {
  background: #212121 !important;
  color: white !important;
}

/* Animations */
</style>
