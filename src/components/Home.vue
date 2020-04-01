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
  
          <iframe
            src="https://open.spotify.com/embed/track/5hVpPjIWHrS3icQIjMOb3v"
            width="90%"
            height="380"
            frameborder="0"
            allowtransparency="true"
            allow="encrypted-media"
          ></iframe>

          <iframe
            src="https://open.spotify.com/embed/track/4Z0SznvLhlEQ5qRHxqFe8d"
            width="90%"
            height="380"
            frameborder="0"
            allowtransparency="true"
            allow="encrypted-media"
          ></iframe>

          <iframe
            src="https://open.spotify.com/embed/track/5SCztdGLUnkYMB47qEyDNA"
            width="90%"
            height="380"
            frameborder="0"
            allowtransparency="true"
            allow="encrypted-media"
          ></iframe>

          <iframe
            src="https://open.spotify.com/embed/track/2VCU5KT8IC4EyYFati0W8U"
            width="90%"
            height="380"
            frameborder="0"
            allowtransparency="true"
            allow="encrypted-media"
          ></iframe>
        </v-content>
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
