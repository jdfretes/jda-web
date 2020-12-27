<template>
  <v-app-bar app color="white" style="position: relative" flat>
    
    <v-tabs centered class="ml-n9" color="grey darken-1">
      <v-tab v-for="link in links" :key="link">
        {{ link }}
      </v-tab>
    </v-tabs>

  </v-app-bar>
</template>
<script>
export default {
  name: "NavigationBar",

  data: () => ({
    links: ["Home"],
  }),
  methods: {
    
  },
};
</script>

<style>
.page-title {
  font-size: 2rem !important;
}
</style>