<template>
  <v-container>
    <NavigationBar/>
  </v-container>
</template>

<script>
import NavigationBar from "./NavigationBar.vue";
export default {
  name: "Home",
   components: {
    NavigationBar,
  },
  data: () => ({})
};
</script>
