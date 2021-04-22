<template>
  <v-container>
    <v-card>
      <v-card-title>My work experience </v-card-title>
      <v-container fluid>
        <v-row dense>
          <v-col v-for="card in items" :key="card.name">
            <v-card shaped elevation="2">
              <v-img :src="card.src" :aspect-ratio="16 / 9"></v-img>
              <v-card-title v-text="card.name"></v-card-title>
              <v-card-subtitle v-text="card.time"></v-card-subtitle>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn icon @click="card.show = !card.show">
                  <v-icon>{{
                    card.show ? "mdi-chevron-up" : "mdi-chevron-down"
                  }}</v-icon>
                </v-btn>
              </v-card-actions>
              <v-expand-transition>
                <div v-show="card.show">
                  <v-divider></v-divider>
                  <v-card-text>
                    {{ card.description }}
                  </v-card-text>
                </div>
              </v-expand-transition>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "Experience",
  data() {
    return {
      items: [
        {
          name: "Globo",
          time: "Jan 2017 - Dec 2018",
          src: require("@/assets/images/experience/globo.jpg"),
          show: false,
          description: "TBD",
        },
        {
          name: "Meta",
          time: "Jan 2019 - Nov 2019",
          src: require("@/assets/images/experience/meta.png"),
          show: false,
          description: "TBD",
        },
        {
          name: "Cyberlabs",
          time: "Dez 2019 - Oct 2020",
          src: require("@/assets/images/experience/cyberlabs.png"),
          show: false,
          description: "TBD",
        },
        {
          name: "Sensedia",
          time: "Nov 2020 - Feb 2021",
          src: require("@/assets/images/experience/sensedia.png"),
          show: false,
          description: "TBD",
        },
        {
          name: "Zé Delivery",
          time: "Apr 2021 - Present",
          src: require("@/assets/images/experience/zedelivery.jpg"),
          show: false,
          description: "TBD",
        },
      ].reverse(),
    };
  },
};
</script>