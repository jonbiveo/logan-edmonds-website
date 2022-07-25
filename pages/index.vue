<template>
  <div>
    <HomeCard />
    <v-card text class="transparent" elevation="0" min-height="200px"></v-card>
    <MainCard />
  </div>
</template>

<script>
import HomeCard from "../components/Home/HomeCard.vue"
import MainCard from "../components/Home/MainCards.vue"
export default {
  name: 'IndexPage',
  components: {
    HomeCard,
    MainCard
  }
}
</script>