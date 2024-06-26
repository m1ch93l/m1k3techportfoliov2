<template>
  <v-sheet color="#0d1117" elevation="3" rounded="lg">
    <v-tabs v-model="tab" :items="tabs" align-tabs="center" color="white" height="60" slider-color="#f78166">
      <template v-slot:tab="{ item }">
        <v-tab :prepend-icon="item.icon" :text="item.text" :value="item.value" class="text-none"></v-tab>
      </template>

      <template v-slot:item="{ item }">
        <YourPageComponent v-if="item.value === 'tab-1'" />
        <AnotherPageComponent v-if="item.value === 'tab-2'" />
        <YourThirdPageComponent v-if="item.value === 'tab-3'" />
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
        icon: 'mdi-book-open-page-variant',
        text: 'Readme',
        value: 'tab-1',
      },
      {
        icon: 'mdi-handshake-outline',
        text: 'Code of Conduct',
        value: 'tab-2',
      },
      {
        icon: 'mdi-license',
        text: 'MIT License',
        value: 'tab-3',
      },
    ],
  }),
}
</script>
