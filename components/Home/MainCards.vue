<template>
  <v-card class="mx-auto" max-width="1200px">
    <v-row class="mb-6">
      <v-col cols="12">
        <v-card class="mx-auto cyan darken-3" max-width="800px">
          <v-card-title class="headline justify-center">
            Welcome to my personal website
          </v-card-title>
        </v-card>
      </v-col>
      <v-col v-for="card in cards" :key="card.id" :cols="card.cols" :sm="card.sm" :lg="card.lg" :xl="card.xl">
        <v-card class="mx-4 cyan darken-4" min-height="100px">
          <v-card-actions class="justify-center">
            <v-btn outlined :to="card.link">
              {{ card.text }}
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  name: 'MainCards',
  data() {
    return {
      cards: [
        {
          cols: '12',
          sm: '6',
          lg: '6',
          xl: '6',
          link: './About',
          text: 'About'
        },
        {
          cols: '12',
          sm: '6',
          lg: '6',
          xl: '6',
          link: './Resume',
          text: 'Resume'
        },
        {
          cols: '12',
          sm: '6',
          lg: '4',
          xl: '4',
          link: '',
          text: 'Canon Calculators'
        },
        {
          cols: '12',
          sm: '6',
          lg: '4',
          xl: '4',
          link: '',
          text: 'House Planner'
        },
        {
          cols: '12',
          sm: '6',
          lg: '4',
          xl: '4',
          link: '',
          text: 'Crypto Goals'
        },
      ]
    }
  }
}
</script>