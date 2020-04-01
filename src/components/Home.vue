<template>
  <div>
    <NavigationBar />

    <v-content>
      <v-container class="fill-height" fluid>
        <!-- <iframe
          src="//www.beatstars.com/embed/track/?id=4105061"
          width="100%"
          height="140"
          style="border: none; background-color: #"
        ></iframe>-->

        <iframe
          src="https://open.spotify.com/embed/track/5hVpPjIWHrS3icQIjMOb3v"
          width="300"
          height="380"
          frameborder="0"
          allowtransparency="true"
          allow="encrypted-media"
        ></iframe>

        <iframe
          src="https://open.spotify.com/embed/track/4Z0SznvLhlEQ5qRHxqFe8d"
          width="300"
          height="380"
          frameborder="0"
          allowtransparency="true"
          allow="encrypted-media"
        ></iframe>

        <iframe
          src="https://open.spotify.com/embed/track/5SCztdGLUnkYMB47qEyDNA"
          width="300"
          height="380"
          frameborder="0"
          allowtransparency="true"
          allow="encrypted-media"
        ></iframe>

        <iframe
          src="https://open.spotify.com/embed/track/2VCU5KT8IC4EyYFati0W8U"
          width="300"
          height="380"
          frameborder="0"
          allowtransparency="true"
          allow="encrypted-media"
        ></iframe>
      </v-container>
    </v-content>

    <v-footer color="indigo" app>
      <span class="white--text">&copy; 2019 JDA</span>
    </v-footer>
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
