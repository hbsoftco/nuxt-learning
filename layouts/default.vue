<template>
  <v-app>
    <v-card flat height="200px" tile>
      <v-toolbar dense>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>

        <v-toolbar-title>Title</v-toolbar-title>

        <v-spacer></v-spacer>

        <v-btn>
          <n-link to="/">
            <span>Home</span>
          </n-link>
        </v-btn>

        <v-btn>
          <n-link to="/about">
            <span>About</span>
          </n-link>
        </v-btn>

        <v-btn>
          <n-link to="/blogs/1">
            <span>Blog</span>
          </n-link>
        </v-btn>

      </v-toolbar>
      <nuxt/>
    </v-card>
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
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
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
