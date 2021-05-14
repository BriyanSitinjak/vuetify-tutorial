<template>
  <v-app>
    <v-main>
      <app-toolbar></app-toolbar>
      <router-view />
      <app-footer></app-footer>
    </v-main>
  </v-app>
</template>

<script>
import AppFooter from "./components/AppFooter.vue";
import AppToolbar from "./components/AppToolbar.vue";

export default {
  name: "App",

  data: () => ({
    //
  }),

  components: {
    AppFooter,
    AppToolbar,
  },
};
</script>
