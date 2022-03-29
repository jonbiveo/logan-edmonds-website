<template>
<!-- v-app id="main" dark :style="{background: $vuetify.theme.themes[theme].background}" -->
  <v-app id="main" dark>
    <v-app-bar
      absolute
      app
      shrink-on-scroll
      dense
      prominent
      flat
      rounded
      transparent
      color="rgba(0, 0, 0, 0)"
    >
      <v-col class="d-inline-flex align-center">
        <v-col class="d-flex justify-center">
          <v-app-bar-title>
            <v-btn outlined to="/" v-text="title"></v-btn>
          </v-app-bar-title>
        </v-col>
        <v-spacer></v-spacer>
        <v-col class="d-flex justify-center">
          <v-btn icon href="https://github.com/jonbiveo" target="_blank"><v-icon>mdi-github</v-icon></v-btn>
          <v-btn icon href="https://www.linkedin.com/in/logantedmonds/"><v-icon>mdi-linkedin</v-icon></v-btn>
          <v-btn icon href="mailto:logantedmonds@gmail.com"><v-icon>mdi-email</v-icon></v-btn>
        </v-col>
      </v-col>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
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
      title: 'Logan Edmonds'
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
  background-image: linear-gradient(to bottom right, rgb(3, 3, 34), rgb(6, 6, 77));
}

</style>