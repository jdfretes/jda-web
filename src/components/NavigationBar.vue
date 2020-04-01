<template>
  <v-app-bar
    absolute
    color="#6A76AB"
    dark
    shrink-on-scroll
    prominent
    src="https://images.unsplash.com/photo-1525362081669-2b476bb628c3?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80"
    fade-img-on-scroll
    scroll-target="#scrolling-techniques-4"
  >
    <template v-slot:img="{ props }">
      <v-img v-bind="props" gradient="to top right, rgba(100,115,201,.7), rgba(25,32,72,.7)"></v-img>
    </template>

    <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->
    <v-spacer></v-spacer>

    <v-toolbar-title class="page-title">JDA beats</v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn icon @click="goToNetwork('spotify')">
      <v-icon>mdi-spotify</v-icon>
    </v-btn>

    <v-btn icon @click="goToNetwork('instagram')">
      <v-icon>mdi-instagram</v-icon>
    </v-btn>

    <v-btn icon @click="goToNetwork('soundcloud')">
      <v-icon>mdi-soundcloud</v-icon>
    </v-btn>

    <v-btn icon @click="goToNetwork('youtube')">
      <v-icon>mdi-youtube</v-icon>
    </v-btn>

    <template v-slot:extension>
      <v-tabs align-with-title>
        <v-tab>Home</v-tab>
        <v-tab>Beats</v-tab>
        <!-- <v-tab>Contact</v-tab> -->
      </v-tabs>
    </template>
  </v-app-bar>
</template>
<script>
export default {
  name: "NavigationBar",

  data: () => ({}),
  methods: {
    goToNetwork(network) {
      switch (network) {
        case "spotify":
          window.open("https://open.spotify.com/artist/6v6MeoRUMeFfKcAyYNEge8", "_self");
          break;
        case "instagram":
          window.open("https://www.instagram.com/jda.beats/", "_self");
          break;
        case "soundcloud":
          window.open("https://soundcloud.com/jda_beats/tracks", "_self");
          break;
        case "youtube":
          window.open("https://www.youtube.com/channel/UCiL8_VpqEWLT-4GIKJKx8IQ", "_self");
          break;

        default:
          break;
      }
    }
  }
};
</script>

<style>
.page-title {
  font-size: 2rem !important;
}
</style>