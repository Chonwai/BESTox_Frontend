<template>
  <div>
    <v-app-bar color="#1C2833" height="96px">
      <v-app-bar-nav-icon
        class="d-md-none"
        color="#FFFFFF"
        @click="drawer = true"
      ></v-app-bar-nav-icon>
      <v-toolbar-title
        ><img class="h-16" src="/images/logo.png" alt="" srcset=""
      /></v-toolbar-title>
      <v-spacer></v-spacer>
      <NavItems class="d-none d-md-block" />
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav>
        <v-list-item link nuxt to="/">
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Home</v-list-item-title>
        </v-list-item>
        <v-list-item link nuxt to="/method">
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Method</v-list-item-title>
        </v-list-item>
        <v-list-item link nuxt to="/method">
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Statistics</v-list-item-title>
        </v-list-item>
        <v-list-item link nuxt to="/help">
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Help</v-list-item-title>
        </v-list-item>
        <v-list-item link nuxt to="/contact">
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Contact</v-list-item-title>
        </v-list-item>
        <v-list-item link href="https://cbbio.online/">
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title>CBBio</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
import NavItems from './NavItems'
export default {
  name: 'AppNav',
  components: {
    NavItems,
  },
  data() {
    return {
      drawer: false,
      group: null,
      fixed: false,
      text: 'center',
    }
  },
}
</script>
