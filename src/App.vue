<template>
  <v-app>
    <v-app-bar
      app
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="http://portlandsquash.org/graphics/logo_racquet_shadow.png"
          transition="scale-transition"
          width="25%"
        />
        <v-spacer></v-spacer>
        <div class="d-flex align-center">
          <h2>hi</h2>
        </div>
        <v-spacer></v-spacer>
        <div class="d-flex align-center">
          <h2>hi</h2>
        </div>
      </div>
      <v-spacer></v-spacer>
      <span class="mr-2">something else</span>
      <v-icon>mdi-open-in-new</v-icon>
    </v-app-bar>
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    //
  }),
};
</script>


