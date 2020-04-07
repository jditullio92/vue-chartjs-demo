<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-toolbar-title>vue-chartjs demo</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-tooltip left>
        <template v-slot:activator="{ on }">
          <v-btn
            icon
            x-large
            href="https://www.npmjs.com/package/vue-chartjs"
            v-on="on"
          >
            <v-icon x-large>mdi-npm</v-icon>
          </v-btn>
        </template>
        <span>vue-chartjs npm website</span>
      </v-tooltip>
    </v-app-bar>

    <v-content style="background-color: rgba(0, 0, 0, 0.065);">
      <Home />
    </v-content>
  </v-app>
</template>

<script>
import Home from './components/Home';

export default {
  name: 'App',

  components: {
    Home,
  },

  data: () => ({
    //
  }),
};
</script>
