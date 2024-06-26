<template>
  <v-sheet color="#0d1117" elevation="3" rounded="lg">
    <v-tabs v-model="tab" align-tabs="center" color="white" height="60" slider-color="#f78166">
      <template v-for="item in tabs" :key="item.route">
        <router-link :to="item.route" class="v-tab text-none" :class="{ 'v-tab--active': tab === item.route }"
          @click="tab = item.route">
          <v-tab :prepend-icon="item.icon">{{ item.text }}</v-tab>
        </router-link>
      </template>
    </v-tabs>
    <v-tabs-window class="pa-4">
      <router-view />
    </v-tabs-window>
  </v-sheet>
</template>

<script setup>
import { ref, watch } from 'vue';
import { useRouter, useRoute } from 'vue-router';

const tab = ref('/index');

const tabs = [
  {
    icon: 'mdi-book-open-page-variant',
    text: 'Readme',
    route: '/',
  },
  {
    icon: 'mdi-handshake-outline',
    text: 'Code of Conduct',
    route: '/another',
  },
  {
    icon: 'mdi-license',
    text: 'MIT License',
    route: '/tab-3',
  },
];

const route = useRoute();
watch(
  () => route.path,
  (newPath) => {
    tab.value = newPath;
  },
  { immediate: true }
);
</script>
