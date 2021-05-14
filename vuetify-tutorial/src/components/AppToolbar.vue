<template>
  <v-app-bar app color="primary lighten-1" dark>
    <div class="d-flex align-center">
      <v-img
        alt="Vuetify Logo"
        class="shrink mr-2"
        contain
        src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
        transition="scale-transition"
        width="40"
      />
    </div>

    <v-spacer></v-spacer>

    <v-btn href="/" text>
      <span>HOME</span>
      <!-- <v-icon large>mdi-home</v-icon> -->
    </v-btn>
    <v-btn href="/about" text>
      <span>ABOUT</span>
    </v-btn>
    <router-link to="/login">
      <v-btn text>LOGIN</v-btn>
      <!-- text stands for dissapear the background of button -->
    </router-link>
  </v-app-bar>
</template>