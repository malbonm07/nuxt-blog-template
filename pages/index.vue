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


  <v-container grid-list-xs>
    <v-layout justify-center>
      <v-flex xs12 >
        <h2 class="display-1 pb-3">ABOUT US</h2>
        <p class="subheading font-weight-light">Lorem ipsum dolor sit amet, consectetur   adipiscing elit. Nunc ut tortor tellus. Donec maximus curs us pulvinar. Proin   vehicula eros mauris, sit amet rutrum libero vestibulum ac. Morbi ullamcorper eu  lacus vulputate consect. Etur vivamus sagittis accumsan quam eu malesuada. Proin et  ante vel libero ultrices cursus. Donec felis leo, cu rsus eget hendrerit at, congue  nec enim.</p>
      </v-flex>
    </v-layout>
  </v-container>

    <v-layout row wrap style="background: #E1D1A9;">
      <v-flex xs12 md6>
        <v-card elevation="0" class="pa-2" color="transparent">
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
            <v-btn dark large color="#183759" class="ml-0 marginTop"
            >
            SUBSCRIBE
            </v-btn> 
          </v-flex>
        </v-layout>
          </v-card-text>
        </v-card>        
      </v-flex>
      <v-flex xs12 md6>
        <v-card elevation="0" class="pa-2" color="transparent">
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
<!-- style="background: #D1B370;" -->
      <v-layout row wrap>
        <v-flex xs12 md4>
          <h3 class="mb-2">ON INSTAGRAM</h3>
            <v-layout row wrap>
                <v-flex
                  v-for="n in 6"
                  :key="n"
                  xs4
                  d-flex
                  pa-2
                >
                  <v-card flat tile class="d-flex" nuxt to="/">
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
            <v-flex xs12>
              <v-card elevation="0">
                <v-list>
                  <v-list-tile avatar>
                    <v-list-tile-avatar>
                      <v-img 
                      src="https://picsum.photos/500/300?image=35"
                      class="noBorderRadius"
                      />
                    </v-list-tile-avatar>
                    <v-list-tile-content>
                      <v-list-tile-title>Article Title</v-list-tile-title>
                      <v-list-tile-sub-title>January, 18-2019</v-list-tile-sub-title>
                    </v-list-tile-content>
                  </v-list-tile>
                </v-list>
              </v-card>
            </v-flex>
            <v-flex xs12>
              <v-card elevation="0">
                <v-list>
                  <v-list-tile avatar>
                    <v-list-tile-avatar>
                      <v-img 
                      src="https://picsum.photos/500/300?image=45"
                      class="noBorderRadius"
                      />
                    </v-list-tile-avatar>
                    <v-list-tile-content>
                      <v-list-tile-title>Article Title</v-list-tile-title>
                      <v-list-tile-sub-title>January, 18-2019</v-list-tile-sub-title>
                    </v-list-tile-content>
                  </v-list-tile>
                </v-list>
              </v-card>
            </v-flex>
            <v-flex xs12>
              <v-card elevation="0">
                <v-list>
                  <v-list-tile avatar>
                    <v-list-tile-avatar>
                      <v-img 
                      src="https://picsum.photos/500/300?image=25"
                      class="noBorderRadius"
                      />
                    </v-list-tile-avatar>
                    <v-list-tile-content>
                      <v-list-tile-title>Article Title</v-list-tile-title>
                      <v-list-tile-sub-title>January, 18-2019</v-list-tile-sub-title>
                    </v-list-tile-content>
                  </v-list-tile>
                </v-list>
              </v-card>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex xs12 md4>
          <h3 class="mb-2">TAGS</h3>
          <v-layout row wrap>
            <v-flex shrink>
              <v-chip label color="#183759" text-color="white">
                <v-icon left>label</v-icon>Travel
              </v-chip>
            </v-flex>
            <v-flex shrink>
              <v-chip label color="#183759" text-color="white">
                <v-icon left>label</v-icon>Leisure
              </v-chip>
            </v-flex>
            <v-flex shrink>
              <v-chip label color="#183759" text-color="white">
                <v-icon left>label</v-icon>Political
              </v-chip>
            </v-flex>
            <v-flex shrink>
              <v-chip label color="#183759" text-color="white">
                <v-icon left>label</v-icon>Cooking
              </v-chip>
            </v-flex>
          </v-layout>
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
        { title: 'the art of travel', src: 'https://images.pexels.com/photos/2356045/pexels-photo-2356045.jpeg?auto=format%2Ccompress&cs=tinysrgb&h=750&w=1260', flex: 12, link: '/' },
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
