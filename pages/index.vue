<template>
  <v-app dark>
    <v-container>
      <v-row>
        <v-col md="8">
          <v-card class="pa-10" max-width="fit-content"
            ><h1 class="justify-center">Raph Santana</h1>
            <h2>Software Developer</h2>
            <v-hover v-slot="{ hover }">
              <v-img
                contain
                max-height="300"
                max-width="300"
                src="https://media.discordapp.net/attachments/869071759469608991/903778712263229450/20181231_221941.jpg?width=543&height=543"
                ><v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out black darken-2 v-card--reveal text-h2 white--text"
                    style="height: 100%"
                  >
                    <v-img
                      contain
                      max-height="300"
                      max-width="300"
                      src="https://cdn.discordapp.com/attachments/745075888529342474/938326450254278666/20211025_093631.jpg"
                    ></v-img>
                  </div> </v-expand-transition
              ></v-img>
            </v-hover>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col md="8">
          <v-card class="pa-10">
            <v-list-item two-line>
              <v-list-item-content>
                <v-list-item-title>Senior @ CCC</v-list-item-title>
                <v-list-item-subtitle
                  >Application Programming Major</v-list-item-subtitle
                >
              </v-list-item-content>
            </v-list-item>
            <v-list-item two-line>
              <v-list-item-content>
                <v-list-item-title
                  >Born In Caracas, Venezuela
                </v-list-item-title>
                <v-list-item-subtitle
                  >Living in Chicago since 2018</v-list-item-subtitle
                >
              </v-list-item-content>
            </v-list-item>
            <div class="text-center">
              <v-menu offset-y>
                <template v-slot:activator="{ on, attrs }">
                  <v-btn color="primary" dark v-bind="attrs" v-on="on">
                    Links to my works
                  </v-btn>
                </template>
                <v-list>
                  <v-list-item v-for="(item, index) in items" :key="index">
                    <v-list-item-title
                      ><a :href="item.link">{{
                        item.title
                      }}</a></v-list-item-title
                    >
                  </v-list-item>
                </v-list>
              </v-menu>
            </div>
          </v-card></v-col
        >
        <v-col>
          <v-card class="pa-10">
            <h2>Skills:</h2>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>Javascript / Node</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>ReactJS</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>C#</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>HTML/CSS</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <h2>Learning:</h2>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>Vue/Nuxt</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>Express.js</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>Fastify</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>MongoDB/Mongoose</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col md="8">
          <v-card class="pa-10">
            <h1>Useless info about me:</h1>
            <v-list-item three-line>
              <v-list-item-content>
                <v-list-item-title
                  >The Layout of these cards is supposed to look like
                  this.</v-list-item-title
                >
                <v-list-item-subtitle>
                  I swear that I know how to make grids in CSS...
                </v-list-item-subtitle>
                <v-list-item-subtitle> believe me.</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title
                  >My favorite video games are the Pokémon
                  games.</v-list-item-title
                >
              </v-list-item-content>
            </v-list-item>
            <v-list-item two-line>
              <v-list-item-content>
                <v-list-item-title
                  >I have a severe addiction to Final Fantasy
                  14</v-list-item-title
                >
                <v-list-item-subtitle>I think I need help</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      items: [
        {
          title: 'Parkway',
          link: 'https://national-park-web-app-steel.vercel.app/',
        },
        {
          title: "Silly website I'm working on (React)",
          link: 'https://Raphsant.me',
        },
        {
          title: 'My Github I guess',
          link: 'https://Github.com/Raphsant',
        },
      ],
    }
  },
}
</script>
