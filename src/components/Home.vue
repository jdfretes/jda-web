<template>
  <div>
    <NavigationBar />

    <v-main class="grey lighten-3 top-separator">
      <v-container>
        <v-row>
          <v-col cols="12" sm="2" class="">
            <v-sheet rounded="lg" min-height="auto" class="center">
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
            </v-sheet>
          </v-col>

          <v-col cols="12" sm="8" class="">
            <v-sheet min-height="auto" rounded="lg">
              <v-carousel
                height="400"
                hide-delimiter-background
                show-arrows-on-hover
              >
                <v-carousel-item v-for="(slide, i) in slides" :key="i">
                  <v-sheet :color="slide.color" height="100%">
                    <v-row class="fill-height" align="center" justify="center">
                      <div  class="display-3">
                        <iframe
                          width="560"
                          height="315"
                          :src="slide.url"
                          frameborder="0"
                          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                          allowfullscreen
                        ></iframe>
                      </div>
                    </v-row>
                  </v-sheet>
                </v-carousel-item>
              </v-carousel>

              <v-card max-width="auto" class="mx-auto">
                <v-row dense>
                  <v-col v-for="(item, i) in items" :key="i" cols="12">
                    <v-card :color="item.color" dark>
                      <div class="d-flex flex-no-wrap justify-space-between">
                        <div>
                          <v-card-title
                            class="headline"
                            v-text="item.title"
                          ></v-card-title>

                          <v-card-subtitle
                            v-text="item.artist"
                          ></v-card-subtitle>

                          <v-card-actions>
                            <v-btn
                              class="ml-2 mt-3"
                              fab
                              icon
                              height="40px"
                              right
                              width="40px"
                              @click="onPlay(item.product_link)"
                            >
                              <v-icon>mdi-play</v-icon>
                            </v-btn>

                            <v-btn
                              class="ml-2 mt-3"
                              fab
                              icon
                              height="40px"
                              right
                              width="40px"
                              @click="onPurchase(item.product_link)"
                            >
                              <v-icon>mdi-cart</v-icon>
                            </v-btn>

                            <v-btn
                              class="ml-2 mt-3"
                              fab
                              icon
                              height="40px"
                              right
                              width="40px"
                              @click="onDownload(item.product_link)"
                            >
                              <v-icon>mdi-download</v-icon>
                            </v-btn>
                          </v-card-actions>
                        </div>

                        <v-avatar class="ma-3" size="125" tile>
                          <v-img :src="item.src"></v-img>
                        </v-avatar>
                      </div>
                    </v-card>
                  </v-col>
                </v-row>
              </v-card>
            </v-sheet>
          </v-col>

          <v-col cols="12" sm="2" class="">
            <v-sheet rounded="lg" min-height="auto"> </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </div>
</template>

<script>
import NavigationBar from "./NavigationBar.vue";
export default {
  name: "Home",
  props: {
    source: String,
  },
  components: {
    NavigationBar,
  },
  data: () => ({
    slides: [
      {
        url: "https://www.youtube.com/embed/CqJ4ForQlqg?controls=0",
        color: "#03164B",
      },
      {
        url: "https://www.youtube.com/embed/6H_8dJNLUNI?controls=0",
        color: "#616161",
      },
    ],
    items: [
      {
        color: "#511C80",
        src:
          "https://cdn.beatstars.com/eyJidWNrZXQiOiJidHMtY29udGVudCIsImtleSI6InVzZXJzL3Byb2QvMTQ5OTUyNy9pdzUxanl2c3IucG5nIiwiZWRpdHMiOnsicmVzaXplIjp7ImZpdCI6bnVsbCwid2lkdGgiOjIwMCwiaGVpZ2h0IjoyMDB9fX0=",
        title: "Sensaciones [Dance Hall] Sky rompiendo Type beat",
        artist: "JDA beats",
        product_link: "https://bsta.rs/6487bd6e",
      },
      {
        color: "#6B4559",
        src:
          "https://cdn.beatstars.com/eyJidWNrZXQiOiJidHMtY29udGVudCIsImtleSI6InVzZXJzL3Byb2QvMTQ5OTUyNy9pdzUxajRkdWQuanBnIiwiZWRpdHMiOnsicmVzaXplIjp7ImZpdCI6bnVsbCwid2lkdGgiOjIwMCwiaGVpZ2h0IjoyMDB9fX0=",
        title: "LUV(EMOTIONAL LOFI TRAP)",
        artist: "JDA beats",
        product_link: "https://bsta.rs/2e282c4c",
      },
    ],
  }),
  methods: {
    goToNetwork(network) {
      switch (network) {
        case "spotify":
          window.open(
            "https://open.spotify.com/artist/6v6MeoRUMeFfKcAyYNEge8",
            "_self"
          );
          break;
        case "instagram":
          window.open("https://www.instagram.com/jda.beats/", "_self");
          break;
        case "soundcloud":
          window.open("https://soundcloud.com/jda_beats/tracks", "_self");
          break;
        case "youtube":
          window.open(
            "https://www.youtube.com/channel/UCiL8_VpqEWLT-4GIKJKx8IQ",
            "_self"
          );
          break;

        default:
          break;
      }
    },
    onPlay(url) {
      window.open(url, "_blank");
    },
    onPurchase(url) {
      window.open(url, "_blank");
    },
    onDownload(url) {
      window.open(url, "_blank");
    },
  },
};
</script>
<style>
.bg-orange {
  background-color: orange;
}

.bg-darkkhaki {
  background-color: darkkhaki;
}

.bg-hotpink {
  background-color: hotpink;
}
.top-separator {
  margin-top: 32px;
}

.center {
  text-align: center;
}
</style>
