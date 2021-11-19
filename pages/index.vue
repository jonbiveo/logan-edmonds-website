<template>
  <v-container>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="8" md="6">
        <v-card>
          <v-card-title class="headline">
            Welcome to my personal website
          </v-card-title>
          <v-card-text>
            Hello
            <v-icon >mdi-bitcoin</v-icon>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-row justify="center" align="center" class="mb-6">
      <v-col md="4">
        <v-card class=" pa-2" max-width="400px">
          <v-card-actions class="justify-center">
            <v-btn to="./about">
              About
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col md="4">
        <v-card class="pa-2" max-width="400px">
          <v-card-actions class="justify-center">
            <v-btn to="./resume">
              Resume
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style>

</style>