<template>
  <v-container>
    <v-carousel cycle :show-arrows="false">
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item"
        transition="fade-transition"
      >
      </v-carousel-item>
    </v-carousel>
  </v-container>
</template>

<script>
export default {
  name: "Hero",
  data() {
    return {
      items: [
        require("@/assets/images/01.jpeg"),
        require("@/assets/images/02.jpeg"),
        require("@/assets/images/03.jpeg"),
      ],
    };
  },
};
</script>
