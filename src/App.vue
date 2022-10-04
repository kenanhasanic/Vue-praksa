<template>
  <v-app>
    <v-container>

      <Header />
      <div class="paddingDiv"></div>
      <router-view></router-view>

    </v-container>
  </v-app>
</template>


<script>
import Header from './components/Header/Header.vue'
export default {
  name: 'App',
  components: {
    Header
  },
  data: () => ({
    drawer: false,
    items: [
      { title: 'View Meetups', icon: 'mdi-account-group' },
      { title: 'Organize Meetup', icon: 'mdi-map-marker' },
      { title: 'Profile', icon: 'mdi-account' },
      { title: 'Sign up', icon: 'mdi-face' },
      { title: 'Sign in', icon: 'mdi-lock-open' },
    ],
  }),
};
</script>


<style>
  .paddingDiv{
    padding-top: 100px
  }
</style>

