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
    >
      <v-toolbar-side-icon @click="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
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


    <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; 2019</span>
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
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'bubble_chart',
          title: 'Inspire',
          to: '/inspire'
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
