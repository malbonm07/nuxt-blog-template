<template>
  <v-app>

<!--------------------------- TOOLBAR --------------------------->

    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-tile
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title" />
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar
      :clipped-left="clipped"
      fixed
      app
      height="70px"
      flat
    >
      <v-toolbar-side-icon @click="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn router to="/" flat>Home</v-btn>
          <v-btn router to="travel" flat>Travel</v-btn>
          <v-btn flat>Leisure</v-btn>
          <v-btn flat>Blog</v-btn>
        </v-toolbar-items>
        <v-text-field
            background-color="#E0E0E0"
            flat
            clearable
            height="47px"
            solo
            label="Search"
            append-icon="place"
        >
        </v-text-field>
    </v-toolbar>

<!--------------------------- END TOOLBAR --------------------------->

<!--------------------------- PAGE VIEW --------------------------->

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

<!--------------------------- END PAGE VIEW --------------------------->

<!--------------------------- FOOTER --------------------------->
    <div style="background: #202020;" class="pt-5 pb-5" id="footer"> 
      <v-layout row wrap class="mb-4" justify-center>
          <div>
            <v-btn fab small color="#D1B370" class="noBorderRadius">
              <font-awesome-icon :icon="['fab', 'linkedin-in']" style="font-size: 18px;"/>
            </v-btn>
          </div>
          <div>
            <v-btn fab small color="#D1B370" class="noBorderRadius">
              <font-awesome-icon :icon="['fab', 'twitter']" style="font-size: 18px;"/>
            </v-btn>
          </div>
          <div>
            <v-btn fab small color="#D1B370" class="noBorderRadius">
              <font-awesome-icon :icon="['fab', 'instagram']" style="font-size: 18px;"/>
            </v-btn>
          </div>
          <div>
            <v-btn fab small color="#D1B370" class="noBorderRadius">
              <font-awesome-icon :icon="['fab', 'facebook-f']" style="font-size: 18px;"/>
            </v-btn>
          </div>
          <div>
            <v-btn fab small color="#D1B370" class="noBorderRadius">
              <font-awesome-icon :icon="['fab', 'twitch']" style="font-size: 18px;"/>
            </v-btn>
          </div>
          <div>
            <v-btn fab small color="#D1B370" class="noBorderRadius">
              <font-awesome-icon :icon="['fab', 'reddit']" style="font-size: 18px;"/>
            </v-btn>
          </div>
          <div>
            <v-btn fab small color="#D1B370" class="noBorderRadius">
              <font-awesome-icon :icon="['fab', 'pinterest']" style="font-size: 18px;"/>
            </v-btn>
          </div>
      </v-layout>
    </div>

    <v-footer
      :fixed="fixed"
      app
    >
    <v-layout row wrap justify-center>
      <v-flex shrink>
        <span class="text-xs-center caption">&copy; 2019 Personal Blog. All Rights Reserved.</span>
      </v-flex>
    </v-layout>
    </v-footer>

<!--------------------------- END FOOTER --------------------------->

  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'apps',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'flight_takeoff',
          title: 'Travel',
          to: '/travel'
        },
        {
          icon: 'rowing',
          title: 'Leisure',
          to: '/leisure'
        },
        {
          icon: 'book',
          title: 'Blog',
          to: '/blog'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
