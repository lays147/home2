<template>
  <div id="id">
    <v-app>
      <v-app-bar elevate-on-scroll prominent color="deep-purple darken-2">
        <v-toolbar-title class="white--text"
          >Lays Rodrigues | Software Engineer
        </v-toolbar-title>
      </v-app-bar>
      <v-container>
        <Technologies />
        <Hero />
        <Experience />
      </v-container>
    </v-app>
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Experience from "./components/Experience.vue";
import Technologies from "./components/Technologies.vue";

export default {
  name: "App",
  components: {
    Hero,
    Experience,
    Technologies,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
