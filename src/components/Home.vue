<template>
  <div>
    <NavigationBar />

    <v-content>
      <v-container class="fill-height" fluid>
        <v-content style="margin-left:5%; margin-right:5%;">
          <iframe
            src="//www.beatstars.com/embed/track/?id=4105061"
            width="90%"
            height="140"
            style="border: none;"
          ></iframe>
      
        </v-content>
      </v-container>
    </v-content>
  </div>
</template>

<script>
import NavigationBar from "./NavigationBar.vue";
export default {
  name: "Home",
  props: {
    source: String
  },
  components: {
    NavigationBar
  },
  data: () => ({})
};
</script>
