<template>
  <v-container class="mb-12">
    <v-row class="mt-12" justify="center">
      <v-col cols="12" md="6" lg="6" xl="6" class="d-flex justify-center align-center">
        <v-card width="auto" class="justify-center">
          <v-img 
          :src="require('~/assets/Edmonds_Logan.jpg')"
          contain
          width="auto"
          max-width="400px"
          ></v-img>
        </v-card>
      </v-col>
      <v-col cols="12" md="6" lg="6" xl="6"  class="d-flex align-center justify-center mx-n12">
        <div>
          <v-card-text class="text-center">
            Hello, my name is
          </v-card-text>
          <v-card-title id="title" class="text-h4 justify-center" >
            Logan Edmonds
          </v-card-title>
          <v-card-text class="text-center">
            A Full-stack Bootcamp Graduate
          </v-card-text>
          <v-card-text class="text-center">
            <v-btn
            icon
            href="https://github.com/jonbiveo"
            target="_blank"
            class="pt-1"
            ><v-icon>mdi-github</v-icon></v-btn>
              <v-divider
              class="mx-2 pb-3"
              vertical
              style="display: inline;"
              ></v-divider>
            <v-btn
            icon
            href="https://www.linkedin.com/in/logantedmonds/"
            target="_blank"
            class="pt-1"
            ><v-icon>mdi-linkedin</v-icon></v-btn>
              <v-divider
              class="mx-2 pb-3"
              vertical
              style="display: inline;"
              ></v-divider>
            <v-btn
            icon
            href="mailto:logantedmonds@gmail.com"
            class="pt-1"
            ><v-icon>mdi-email</v-icon></v-btn>
          </v-card-text>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'HomeCard'
}
</script>

<style>

#title {
  word-break: break-word;
  text-align: center;
}

</style>