<template>
  <v-card class="mx-auto transparent" flat max-width="1200px">
    <v-row class="mb-6">
      <v-col v-for="card in cards" :key="card.id" :cols="card.cols" :sm="card.sm" :lg="card.lg" :xl="card.xl">
        <v-card class="cardsBG mx-4">
          <v-card-actions class="cardsBG justify-center">
            <v-btn text class="transparent" elevation="0" :href="card.link" target="_blank">
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

<style>

.cardsBG {
  background: rgba(124, 232, 252, 0.15);
  -webkit-backdrop-filter: blur(10px);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(70,254,192,0.1);
}

</style>
