<template>
  <v-sheet color="#0d1117" elevation="3" rounded="lg">
    <v-tabs v-model="tab" :items="tabs" align-tabs="center" color="white" height="60" slider-color="#f78166">
      <template v-slot:tab="{ item }">
        <v-tab :prepend-icon="item.icon" :text="item.text" :value="item.value" class="text-none"></v-tab>
      </template>

      <!-- Replace the content of the tabs with your own page components -->
      <template v-slot:item="{ item }">
        <v-tabs-window-item :value="item.value" class="pa-4">
          <!-- Replace this placeholder content with your own page component -->
          <Profile v-if="item.value === 'tab-1'" />
          <Projects v-if="item.value === 'tab-2'" />
          <Contact v-if="item.value === 'tab-3'" />
        </v-tabs-window-item>
      </template>
    </v-tabs>
  </v-sheet>
</template>

<script>

export default {
  data: () => ({
    tab: 'tab-1',
    tabs: [
      {
        icon: 'mdi-account',
        text: 'Profile',
        value: 'tab-1',
      },
      {
        icon: 'mdi-coffee',
        text: 'Projects',
        value: 'tab-2',
      },
      {
        icon: 'mdi-phone',
        text: 'Contact',
        value: 'tab-3',
      },
    ],
  }),
}
</script>
