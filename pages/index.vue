<template>
  <v-card class="mx-auto" max-width="940px">
    <v-container fluid>
      <v-row class="mb-6">
        <v-col cols="12">
          <v-card class="mx-auto cyan darken-3" max-width="500px">
            <v-card-title class="headline justify-center">
              Logan Edmonds
            </v-card-title>
          </v-card>
        </v-col>
        <v-col lg="6" sm="6" xs="12">
          <v-card class="mx-auto pa-2 cyan darken-4" min-height="340px" max-width="300px">
            <v-card-actions class="justify-center px-16 mx-12">
              <v-btn outlined to="./about">
                About
              </v-btn>
            </v-card-actions>
            <div class="text-center">
              <v-icon>mdi-language-javascript</v-icon>
              <v-icon>mdi-language-java</v-icon>
              <v-icon>mdi-vuejs</v-icon>
              <v-icon>mdi-react</v-icon>
              <v-icon>mdi-nuxt</v-icon>
              <v-icon>mdi-nodejs</v-icon>
              <v-icon>mdi-language-html5</v-icon>
              <v-icon>mdi-language-css3</v-icon>
              <v-icon>mdi-bootstrap</v-icon>
              <v-icon>mdi-vuetify</v-icon>
            </div>
          </v-card>
        </v-col>
        <v-col lg="6" sm="6" xs="12">
          <v-card class="mx-auto pa-2 cyan darken-4" min-height="340px" max-width="300px">
            <v-card-actions class="justify-center px-16 mx-12">
              <v-btn outlined to="./resume">
                Resume
              </v-btn>
            </v-card-actions>
            <v-img contain :src="resumeSrc" max-height="260px" max-width="250px" class="mx-auto"></v-img>
          </v-card>
        </v-col>
        <v-col lg="4" sm="6" xs="12">
          <v-card class="mx-auto pa-2 cyan darken-4" min-height="340px" max-width="300px">
            <v-card-actions class="justify-center px-16">
              <v-btn outlined href="https://github.com/jonbiveo/Canon-Calculators">
                Canon Calculators
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col lg="4" sm="6" xs="12">
          <v-card class="mx-auto pa-2 cyan darken-4" min-height="340px" max-width="300px">
            <v-card-actions class="justify-center px-16">
              <v-btn outlined href="https://github.com/jonbiveo/house-planner">
                House Planner
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col lg="4" sm="6" xs="12">
          <v-card class="mx-auto pa-2 cyan darken-4" min-height="340px" max-width="300px">
            <v-card-actions class="justify-center px-16">
              <v-btn outlined href="https://github.com/Tuxman/crypto-goals">
                Crypto Goals
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col lg="6" sm="6" xs="12">
          <v-card class="mx-auto pa-2 cyan darken-4" min-height="340px" max-width="300px">
            <v-card-actions class="justify-center px-16">
              <v-btn outlined href="https://github.com/jonbiveo/tenmo">
                Tenmo
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col lg="6" sm="6" xs="12">
          <v-card class="mx-auto pa-2 cyan darken-4" min-height="340px" max-width="300px">
            <v-card-actions class="justify-center px-16">
              <v-btn outlined href="https://github.com/jonbiveo/Vending-Machine-CLI">
                Vending Machine CLI
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      resumeSrc: require("@/static/ResumeScreenshot.png")
    }
  }
}
</script>

<style>

</style>