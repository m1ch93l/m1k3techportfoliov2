<template>
  <v-container fluid>
    <v-row>
      <v-col v-for="(card, index) in cards" :key="index" cols="12" md="4">
        <v-hover v-slot="{ isHovering, props }">
          <v-card :class="{ 'on-hover': isHovering, 'mx-auto': true }" :elevation="isHovering ? 12 : 2" v-bind="props" max-width="344">
            <v-img height="200px" :src="card.photo" cover></v-img>

            <v-card-title>
              {{ card.title }}
            </v-card-title>

            <v-card-subtitle>
              {{ card.link }}
            </v-card-subtitle>

            <v-card-actions>
              <v-btn color="orange-lighten-2" text="Explore" :href="card.url"></v-btn>

              <v-spacer></v-spacer>
            </v-card-actions>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: 'Faculty Evaluation System',
          photo: 'src/assets/facultyEvaluationSystem.jpg',
          link: 'facultyevaluation.online',
          url: 'https://github.com/m1ch93l/faculty-evaluation-system-procedural-php',
        },
        {
          title: 'Stock Card System',
          photo: 'src/assets/stock-card-system.png',
          link: 'stock-card-invesys.online',
          url: 'https://github.com/m1ch93l/stock-card-invesys',
        },
        {
          title: 'Class List Group Generator',
          photo: 'src/assets/classlist-group-generator.png',
          link: 'classlist-group-generator.online',
          url: 'https://github.com/m1ch93l/classlist-group-generator',
        },
      ],
      transparent: 'rgba(255, 255, 255, 0)',
    };
  },
};
</script>

<style scoped>
.v-card {
  transition: opacity .4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.6;
}

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
</style>
