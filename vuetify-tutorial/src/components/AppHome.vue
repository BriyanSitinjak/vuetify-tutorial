<template>
  <v-app>
    <v-carousel v-model="model">
      <v-carousel-item v-for="(color, i) in colors" :key="color">
        <v-sheet :color="color" height="100%" tile>
          <v-row class="fill-height" align="center" justify="center">
            <div class="display-3">Slide {{ i + 1 }}</div>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
    <v-card class="mx-auto" max-width="344">
      <v-img
        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
        height="200px"
      ></v-img>
      <v-card-title> Our Best Product </v-card-title>
      <v-card-subtitle>
        Housing Payment dapat membantu anda dalam menyelesaikan kebingungan anda
        dalam merekap biaya rumah anda
      </v-card-subtitle>
      <v-card-actions>
        <v-btn color="grey darken-2"> Explore </v-btn>
      </v-card-actions>
    </v-card>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    model: 0,
    colors: ["primary", "indigo", "yellow darken-2", "brown", "orange"],
  }),
};
</script>