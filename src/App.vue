<template>
  <v-layout class="overflow-visible" style="height: 56px;">
    <v-bottom-navigation v-model="value" color="teal" grow>
      <v-btn>
        <v-icon>mdi-home</v-icon>

        Recents
      </v-btn>

      <v-btn>
        <v-icon>mdi-apps</v-icon>

        Favorites
      </v-btn>

      <v-btn>
        <v-icon>mdi-phone</v-icon>

        Nearby
      </v-btn>
    </v-bottom-navigation>
  </v-layout>
</template>

<script setup>
//
</script>
