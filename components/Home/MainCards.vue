<template>
  <v-card class="mx-auto transparent" flat max-width="1200px">
    <v-row class="mb-6">
      <v-col v-for="card in cards" :key="card.id" :cols="card.cols" :sm="card.sm" :lg="card.lg" :xl="card.xl">
        <v-card class="mx-4 cyan darken-4" min-height="100px">
          <v-card-actions class="justify-center">
            <v-btn flat class="transparent" elevation="0" :href="card.link" target="_blank">
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
          lg: '4',
          xl: '4',
          link: 'https://github.com/Tuxman/NuCarbit',
          text: 'NuCarbit'
        },
        {
          cols: '12',
          sm: '6',
          lg: '4',
          xl: '4',
          link: 'https://github.com/jonbiveo/logan-edmonds-morra',
          text: 'Morra'
        },
        {
          cols: '12',
          sm: '6',
          lg: '4',
          xl: '4',
          link: 'https://github.com/Tuxman/crypto-goals',
          text: 'Crypto Goals Tracker'
        },
        {
          cols: '12',
          sm: '6',
          lg: '4',
          xl: '4',
          link: 'https://github.com/jonbiveo/house-planner',
          text: 'House Planner'
        },
        {
          cols: '12',
          sm: '6',
          lg: '4',
          xl: '4',
          link: 'https://github.com/jonbiveo/tenmo',
          text: 'TEnmo'
        },
        {
          cols: '12',
          sm: '6',
          lg: '4',
          xl: '4',
          link: 'https://github.com/jonbiveo/Viska',
          text: 'Viska'
        },
      ]
    }
  }
}
</script>
