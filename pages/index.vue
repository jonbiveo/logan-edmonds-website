<template>
  <v-card class="mx-auto">
    <v-container>
      <v-row class="mb-6">
        <v-col>
          <v-card class="mx-auto cyan darken-3" max-width="800px">
            <v-card-title class="headline justify-center">
              Welcome to my personal website
            </v-card-title>
          </v-card>
        </v-col>
      </v-row>
      <v-row justify="center" align="center" class="mb-6">
        <v-col>
          <v-card class="pa-2 cyan darken-4" min-height="100px" max-width="400px">
            <v-card-actions class="justify-center">
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
        <v-col>
          <v-card class="pa-2 cyan darken-4" min-height="100px" max-width="400px">
            <v-card-actions class="justify-center">
              <v-btn outlined to="./resume">
                Resume
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
      <v-row justify="center" align="center" class="mb-6">
        <v-col>
          <v-card class="pa-2 cyan darken-4" min-height="100px">
            <v-card-actions class="justify-center">
              <v-btn outlined>
                Canon Calculators
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col>
          <v-card class="pa-2 cyan darken-4" min-height="100px">
            <v-card-actions class="justify-center">
              <v-btn outlined>
                House Planner
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col>
          <v-card class="pa-2 cyan darken-4" min-height="100px">
            <v-card-actions class="justify-center">
              <v-btn outlined>
                Crypto Goals
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
}
</script>

<style>

</style>