<template>
  <v-tabs v-model="tab" align-tabs="center" color="deep-purple-accent-4">
    <v-tab :to="{ path: '/' }">Landscape</v-tab>
    <v-tab :to="{ path: '/city' }">City</v-tab>
    <v-tab :to="{ path: '/abstract' }">Abstract</v-tab>
  </v-tabs>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const tab = ref(null);
    return { tab };
  },
}
</script>
