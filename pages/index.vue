<template>
  <div>
    <HomeCard />
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