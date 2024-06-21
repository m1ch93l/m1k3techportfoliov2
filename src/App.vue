<template>
  <v-layout class="overflow-visible" style="height: 56px;">
    <v-bottom-navigation v-model="value" color="teal" grow>
      <v-btn>
        <v-icon>mdi-account</v-icon>

        Profile
      </v-btn>

      <v-btn>
        <v-icon>mdi-apps</v-icon>

        Projects
      </v-btn>

      <v-btn>
        <v-icon>mdi-phone</v-icon>

        Contact
      </v-btn>
    </v-bottom-navigation>
  </v-layout>
</template>

<script setup>
//
</script>
