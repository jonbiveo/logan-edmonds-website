<template>
  <v-app id="app" dark>
    <v-app-bar
      absolute
      app
      shrink-on-scroll
      dense
      prominent
      flat
      height="200px"
      color="rgba(0, 0, 0, 0)"
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
              <v-btn outlined to="/" v-text="title"></v-btn>
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
            rounded
            small
            class="mr-4"
            to="/About"
            >About</v-btn>
            <v-btn
            rounded
            small
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
    <v-navigation-drawer
    app
    expand-on-hover
    permanent
    color="sidebar"
    >
      <v-list>
        <v-list-item-group>
          <v-list-item
          v-for="nav in sideNav"
          :key="nav.name"
          :to="nav.link"
          >
            <v-list-item-icon>
              <v-icon v-text="nav.icon"></v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title v-text="nav.name"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-main id="main">
      <v-container id="container">
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      app
      inset
      class="justify-center pl-0"
      color="footer"
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
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

#main {
  background: url(~/assets/bg-website.svg);
  position: absolute;
  background-size: cover;
  width: 100%;
  min-height: 85%;
  top: 15%;
  /* background-image: linear-gradient(to bottom right, rgb(3, 3, 34), rgb(6, 6, 77)); */
}

#app {
  background-image: linear-gradient(
  170deg,
  hsl(240deg 88% 3%) 0%,
  hsl(234deg 63% 11%) 20%,
  hsl(226deg 90% 15%) 35%,
  hsl(227deg 97% 21%) 47%,
  hsl(235deg 79% 30%) 56%,
  hsl(244deg 60% 39%) 64%,
  hsl(245deg 44% 47%) 72%,
  hsl(244deg 38% 54%) 81%,
  hsl(243deg 38% 62%) 90%,
  hsl(242deg 36% 69%) 100%);
}

#container {
  max-width: 1200px;
}

</style>