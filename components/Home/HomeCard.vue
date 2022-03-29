<template>
    <v-row class="mt-12" justify="center">
      <v-col cols="4">
        <v-card height="200px">
          <v-card-text class="text-center">Hello</v-card-text>
        </v-card>
      </v-col>
      <v-col cols="1"></v-col>
      <v-col cols="4">
        <v-card-text class="text-center">
          Hello, my name is
        </v-card-text>
        <v-card-title class="text-h4 justify-center" >
          Logan Edmonds
        </v-card-title>
        <v-card-text class="text-center">
          A Java full-stack bootcamp graduate
        </v-card-text>
      </v-col>
    </v-row>
</template>

<script>
export default {
  name: 'HomeCard'
}
</script>