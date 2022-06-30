<template>
  <v-app id="app" :style="{background: $vuetify.theme.themes[theme].background}">
    <v-app-bar
      id="header"
      app
      dense
      flat
      height="90px"
      color="rgba(0,0,0,0)"
    >
      <v-container max-width="1200px" class="d-flex justify-center align-center">
        <v-row justify="center">
          <v-col
          class="d-inline-flex justify-center align-center mt-2"
          cols="12"
          md="3"
          lg="3"
          xl="3"
          >
            <v-app-bar-title>
              <v-btn to="/" outlined>{{ title }}</v-btn>
            </v-app-bar-title>
          </v-col>
          <v-col
          class="d-inline-flex justify-center align-center"
          cols="12"
          md="3"
          lg="3"
          xl="3"
          >
            <v-btn
            plain
            class="mr-4"
            to="/About"
            >About</v-btn>
            <v-btn
            plain
            to="/Resume"
            >Resume</v-btn>
          </v-col>
          <v-col
          class="d-flex justify-center"
          cols="12"
          md="3"
          lg="3"
          xl="3"
          >
            <v-btn icon><v-icon>mdi-weather-night</v-icon></v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-app-bar>
    <v-main id="main">
      <v-container id="container">
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      app
      bottom
      absolute
      class="justify-center pl-0"
      color="background"
    >
      <v-card class="text-center" color="rgba(0,0,0,0)" flat width="90%">
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
        <v-divider></v-divider>
        <v-card-text>
          &copy; {{ new Date().getFullYear() }}
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultView',
  data () {
    return {
      fixed: false,
      title: 'Logan Edmonds',
      sideNav: [
        {
          name: 'Home',
          icon: 'mdi-home-circle-outline',
          link: '/'
        },
        {
          name: 'About',
          icon: 'mdi-account',
          link: '/About'
        },
        {
          name: 'Resume',
          icon: 'mdi-note-text-outline',
          link: '/Resume'
        },
      ]
    }
  },
  computed:{
    theme(){
      return (this.$vuetify.theme.dark) ? 'dark' : 'light'
    }
  }
}
</script>

<style>

*, *::before, *::after {
  box-sizing: border-box;
}

* {
  margin: 0;
}

html, body {
  height: 100%;
}

body {
  line-height: 1.5;
  -webkit-font-smoothing: antialiased;
}

img, picture, video, canvas, svg {
  display: block;
  max-width: 100%;
}

input, button, textarea, select {
  font: inherit;
}

p, h1, h2, h3, h4, h5, h6 {
  overflow-wrap: break-word;
}

#root, #__next {
  isolation: isolate;
}

#container {
  max-width: 1200px;
}

::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-track {
  background: #12161D;
}

::-webkit-scrollbar-thumb {
  background: #888;
  border-radius: 10px;
}

::-webkit-scrollbar-thumb:hover {
  background: #555;
}

</style>
