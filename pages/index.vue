<template>
  <div>
  <v-layout justify-center>
    <v-flex xs12>

          <v-layout row wrap>
            <v-flex
              v-for="card in cards"
              :key="card.title"
              xs12
              v-bind="{ [`md${card.flex}`]: true }"
              class="pa-3"
            >
              <v-card elevation="0">
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
                        <span class="headline white--text" v-text="card.title"></span>
                      </v-flex>
                    </v-layout>
                  </v-container>
                </v-img>

                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn icon>
                    <v-icon>favorite</v-icon>
                  </v-btn>
                  <v-btn icon>
                    <v-icon>bookmark</v-icon>
                  </v-btn>
                  <v-btn icon>
                    <v-icon>share</v-icon>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>

    </v-flex>
  </v-layout>


  <v-container grid-list-xs>
    <v-layout justify-center>
      <v-flex xs12 >
        <h2 class="display-1 pb-3">ABOUT US</h2>
        <p class="subheading font-weight-light">Lorem ipsum dolor sit amet, consectetur   adipiscing elit. Nunc ut tortor tellus. Donec maximus curs us pulvinar. Proin   vehicula eros mauris, sit amet rutrum libero vestibulum ac. Morbi ullamcorper eu  lacus vulputate consect. Etur vivamus sagittis accumsan quam eu malesuada. Proin et  ante vel libero ultrices cursus. Donec felis leo, cu rsus eget hendrerit at, congue  nec enim.</p>
      </v-flex>
    </v-layout>
  </v-container>

    <v-layout row wrap>
      <v-flex xs12 md6>
        <v-card elevation="0" class="pa-2">
          <v-card-title primary-title>
            <h3 class="title">SUSCRIBE</h3>
          </v-card-title>
          <v-card-text>
            <p class="body-1">Enter your email address to subscribe to this blog and receive notifications of new posts by email.</p>
        <v-layout>
          <v-flex xs8>
          <v-text-field
            background-color="#E0E0E0"
            flat
            clearable
            solo
            height="46px"
          >
          </v-text-field>            
          </v-flex>
          <v-flex xs4>
            <v-btn dark large color="#263238" class="ml-0 marginTop"
            >
            SUBSCRIBE
            </v-btn> 
          </v-flex>
        </v-layout>
          </v-card-text>
        </v-card>        
      </v-flex>
      <v-flex xs12 md6>
        <v-card elevation="0" class="pa-2">
          <v-card-title primary-title>
            <h3 class="title">CONTACT</h3>
          </v-card-title>
          <v-card-text>
        <v-list-tile avatar>
            <v-list-tile-avatar>
              <v-icon>mail_outline</v-icon>
            </v-list-tile-avatar>

            <v-list-tile-content>
              <v-list-tile-title>EMAIL</v-list-tile-title>
            </v-list-tile-content>
            <v-list-tile>
              <span>THEARTOFTRAVEL@GM...</span>
            </v-list-tile>
          </v-list-tile>

        <v-divider></v-divider>

        <v-list-tile
            avatar
          >
            <v-list-tile-avatar>
              <v-icon>place</v-icon>
            </v-list-tile-avatar>

            <v-list-tile-content>
              <v-list-tile-title>ADDRESS</v-list-tile-title>
            </v-list-tile-content>
            <v-list-tile>
              <span>1234 WORLD DR. HERE...</span>
            </v-list-tile>
        </v-list-tile>

          <v-divider></v-divider>

        <v-list-tile
            avatar
          >
            <v-list-tile-avatar>
              <v-icon>phone</v-icon>
            </v-list-tile-avatar>

            <v-list-tile-content>
              <v-list-tile-title>PHONE</v-list-tile-title>
            </v-list-tile-content>
            <v-list-tile>
              <span>555-789-1234</span>
            </v-list-tile>
          </v-list-tile>

          <v-divider></v-divider>

        </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>

    <v-container grid-list-xs>
      <v-layout row wrap>
        <v-flex xs12 md4>
          <h3>ON INSTRAGRAM</h3>
            <v-layout row wrap>
                <v-flex
                  v-for="n in 6"
                  :key="n"
                  xs4
                  d-flex
                  pa-1
                >
                  <v-card flat tile class="d-flex">
                    <v-img
                      :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                      :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                      aspect-ratio="1"
                      class="grey lighten-2"
                    >
                      <template v-slot:placeholder>
                        <v-layout
                          fill-height
                          align-center
                          justify-center
                          ma-0
                        >
                          <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                        </v-layout>
                      </template>
                    </v-img>
                  </v-card>
                </v-flex>
            </v-layout>
        </v-flex>
        <v-flex xs12 md4>
          <h3>NEWEST BLOG POSTS</h3>
          <v-layout row wrap>
            
          </v-layout>
        </v-flex>
        <v-flex xs12 md4>
          
        </v-flex>

      </v-layout>
    </v-container>

  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  },
    data: () => ({
      cards: [
        { title: 'Pre-fab homes', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: 12 },
        { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6 },
        { title: 'Best airlines', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6 },
        { title: 'Pre-fab homes', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: 12 },
        { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6 },
        { title: 'Best airlines', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6 },
        { title: 'Pre-fab homes', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: 4 },
        { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 4 },
        { title: 'Best airlines', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 4 },
        { title: 'Pre-fab homes', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: 4 },
        { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 4 },
        { title: 'Best airlines', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 4 },
      ]
    })
}
</script>
