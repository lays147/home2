<template>
  <v-container>
    <v-card>
      <v-card-title>Technologies</v-card-title>
      <v-container>
        <v-row>
          <v-col v-for="item in items" :key="item">
            <v-chip outlined color="deep-purple darken-3" v-text="item">
            </v-chip>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "Technologies",
  data() {
    return {
      items: [
        "Python",
        "Git",
        "NodeJs",
        "Go",
        "Terraform",
        "Gitlab",
        "C++",
        "Linux",
        "AWS",
        "Docker",
        "ECS",
        "Scrum",
        "Kanban",
        "Infrastructure as Code",
      ].sort(() => Math.random() - 0.5),
    };
  },
};
</script>