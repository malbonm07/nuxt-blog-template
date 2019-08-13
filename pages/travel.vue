<template>
  <v-layout justify-center>
    <v-flex xs12>

          <v-layout row wrap>
            <v-flex
              v-for="(card,index) in cards"
              :key="index"
              xs12
              v-bind="{ [`md${card.flex}`]: true }"
              class="pa-3"
            >
              <v-card elevation="0" :to="card.link" nuxt>
                <v-img
                  :src="card.src"
                  height="350px"
                >
                  <v-container
                    fill-height
                    fluid
                    pa-2
                  >
                    <v-layout fill-height align-center justify-center>
                      <v-flex shrink>
                        <p class="display-2 font-weight-light white--text text-capitalize
                        text-xs-center"
                        >
                        {{card.title}}
                        </p>
                      </v-flex>
                    </v-layout>
                  </v-container>
                </v-img>

                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn icon>
                    <font-awesome-icon :icon="['fab', 'instagram']" style="font-size: 25px;"/>
                  </v-btn>
                  <v-btn icon>
                    <v-icon>share</v-icon>
                  </v-btn>
                  <v-btn small color="#D1B370" dark>
                    Read More
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>

    </v-flex>
  </v-layout>
</template>

<script>
export default {
    data: () => ({
      cards: [
        { title: 'the art of travel', src: 'https://images.pexels.com/photos/338515/pexels-photo-338515.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940', flex: 12, link: '/' },
        { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6, link: '/' },
        { title: 'Best vacations', src: 'https://images.pexels.com/photos/2161449/pexels-photo-2161449.jpeg?auto=format%2Ccompress&cs=tinysrgb&dpr=1&w=500', flex: 6, link: '/' },
        { title: 'Favorite sites', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: 12, link: '/' },
        { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6, link: '/' },
        { title: 'Best experiences', src: 'https://images.pexels.com/photos/2161449/pexels-photo-2161449.jpeg?auto=format%2Ccompress&cs=tinysrgb&dpr=1&w=500', flex: 6, link: '/' },
        { title: 'Cities', src: 'https://images.pexels.com/photos/2076625/pexels-photo-2076625.jpeg?auto=format%2Ccompress&cs=tinysrgb&h=750&w=1260', flex: 4, link: '/' },
        { title: 'Favorite road trips', src: 'https://images.pexels.com/photos/2082103/pexels-photo-2082103.jpeg?auto=format%2Ccompress&cs=tinysrgb&h=750&w=1260', flex: 4, link: '/' },
        { title: 'Best vacations', src: 'https://images.pexels.com/photos/2191851/pexels-photo-2191851.jpeg?auto=format%2Ccompress&cs=tinysrgb&h=750&w=1260', flex: 4, link: '/' },
        { title: 'Independence', src: 'https://images.pexels.com/photos/2249285/pexels-photo-2249285.jpeg?auto=format%2Ccompress&cs=tinysrgb&h=750&w=1260', flex: 4, link: '/' },
        { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 4, link: '/' },
        { title: 'Best adventures', src: 'https://images.pexels.com/photos/2219433/pexels-photo-2219433.jpeg?auto=format%2Ccompress&cs=tinysrgb&h=750&w=1260', flex: 4, link: '/' },
      ]
    })
}
</script>

<style>

</style>
