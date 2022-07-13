<template>
  <v-app id="app" :style="{background: $vuetify.theme.themes[theme].background}">
    <v-app-bar
      id="header"
      app
      dense
      flat
      color="rgba(0,0,0,0)"
      class="mt-4"
    >
      <v-app-bar-nav-icon
      class="d-flex d-sm-none"
      @click="drawer = true"
      ></v-app-bar-nav-icon>
      <v-toolbar-title>
        <v-btn to="/" outlined>{{ title }}</v-btn>
      </v-toolbar-title>
      <v-btn
      plain
      class="mr-4 d-none d-sm-flex"
      to="/About"
      >About</v-btn>
      <v-btn
      plain
      class="d-none d-sm-flex"
      to="/Resume"
      >Resume</v-btn>
      <v-spacer></v-spacer>
      <v-btn class="d-none d-sm-flex" text><v-icon>mdi-weather-night</v-icon></v-btn>      
    </v-app-bar>
    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
        >
          <v-list-item v-for="(item, index) in sideNav" :key="index" class="justify-center">
          <v-btn text :to="item.link">
            <v-list-item-title><v-icon>{{ item.icon }}</v-icon> {{ item.name }}</v-list-item-title>
          </v-btn>
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
      bottom
      absolute
      class="justify-center"
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
      drawer: false,
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
        {
          name: '',
          icon: 'mdi-weather-night',
          link: ''
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
