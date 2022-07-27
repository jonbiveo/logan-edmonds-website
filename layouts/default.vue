<template>
  <v-app
    id="app"
    :style="{background: $vuetify.theme.themes[theme].background}"
  >
    <v-app-bar
      id="header"
      app
      text
      color="rgba(0,0,0,0)"
      fluid
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
        class="d-none d-sm-flex ml-4"
        to="/Resume"
      >
        Resume
      </v-btn>
      <v-menu
        plain
        open-on-hover
        class="d-none d-sm-flex"
      >
        <template #activator="{ on, attrs }">
          <v-btn
            plain
            v-bind="attrs"
            v-on="on"
          >
            Projects
          </v-btn>
        </template>
        <v-list>
          <v-list-item
          v-for="(item, index) in projectNav"
          :key="index"
          >
            <v-btn :href="item.link" target="_blank">{{ item.name }}</v-btn>
          </v-list-item>
        </v-list>
      </v-menu>
      <v-spacer></v-spacer>
      <v-btn
        icon
        class="d-none d-sm-flex"
        @click="toggleTheme"
      >
        <v-icon>{{ $vuetify.theme.dark ? 'mdi-white-balance-sunny' : 'mdi-weather-night' }}</v-icon>
      </v-btn>      
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
          <v-list-item
            v-for="(item, index) in sideNav"
            :key="index"
            class="justify-center"
          >
          <v-btn text :to="item.link">
            <v-list-item-title>
              <v-icon>{{ item.icon }}</v-icon>
              {{ item.name }}
            </v-list-item-title>
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
      <v-card
        class="text-center"
        color="rgba(0,0,0,0)"
        width="90%"
        elevation="0"
        text
      >
        <v-card-text class="text-center">
          <v-btn
            icon
            href="https://github.com/jonbiveo"
            target="_blank"
            class="pt-1"
          >
            <v-icon>mdi-github</v-icon>
          </v-btn>
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
          >
            <v-icon>mdi-linkedin</v-icon>
          </v-btn>
          <v-divider
            class="mx-2 pb-3"
            vertical
            style="display: inline;"
          ></v-divider>
          <v-btn
            icon
            href="mailto:logantedmonds@gmail.com"
            class="pt-1"
          >
            <v-icon>mdi-email</v-icon>
          </v-btn>
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
          name: 'Resume',
          icon: 'mdi-note-text-outline',
          link: '/Resume'
        },
        {
          name: 'Projects',
          icon: 'mdi-account',
          link: '/Projects'
        },
        {
          name: '',
          icon: 'mdi-weather-night',
          link: ''
        }
      ],
      projectNav: [
        {
          name: 'NuCarbit',
          icon: 'mdi-home-circle-outline',
          link: 'https://github.com/Tuxman/NuCarbit'
        },
        {
          name: 'Morra',
          icon: 'mdi-note-text-outline',
          link: 'https://github.com/jonbiveo/logan-edmonds-morra'
        },
        {
          name: 'Crypto Goals',
          icon: 'mdi-account',
          link: 'https://github.com/Tuxman/crypto-goals'
        },
        {
          name: 'House Planner',
          icon: 'mdi-weather-night',
          link: 'https://github.com/jonbiveo/house-planner'
        },
        {
          name: 'Tenmo',
          icon: 'mdi-weather-night',
          link: 'https://github.com/jonbiveo/tenmo'
        },
      ]
    }
  },
  computed:{
    theme(){
      return (this.$vuetify.theme.dark) ? 'dark' : 'light'
    }
  },
  mounted() {
    const theme = localStorage.getItem("dark_theme");
    if (theme) {
      if (theme === "true") {
        this.$vuetify.theme.dark = true;
      } else {
        this.$vuetify.theme.dark = false;
      }
    } else if (window.matchMedia && window.matchMedia("(prefers-color-scheme: dark)").matches) {
      this.$vuetify.theme.dark = true;
      localStorage.setItem("dark_theme", this.$vuetify.theme.dark.toString());
    }
  },
  methods: {
    toggleTheme() {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark;
      localStorage.setItem("dark_theme", this.$vuetify.theme.dark.toString());
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
