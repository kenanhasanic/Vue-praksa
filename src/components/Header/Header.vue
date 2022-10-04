<template>
<v-container>

  <v-app-bar color="primary" class="flex-grow-0" app dark>
      <v-app-bar-nav-icon class="d-lg-none" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title><router-link to="/" style="text-decoration: none; color: inherit;"> Dev Meetups</router-link></v-app-bar-title>
      <v-spacer></v-spacer>
      <div class="d-none d-lg-block">

        <v-btn router :to="item.link" v-for="item in items" :key="item.title" style="text-decoration: none; color: inherit;" class="navButton"> 
          <v-icon right dark style="padding-right: 10px">
            {{ item.icon }}
          </v-icon>
          {{ item.title }}
        </v-btn>

      </div>
    </v-app-bar>
    <v-navigation-drawer class="d-lg-none" app v-model="drawer">
      <v-list dense nav>

        <v-list-item router :to="item.link" v-for="item in items" :key="item.title" link>
            <v-list-item-title>{{ item.title }}
               <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-title>
        </v-list-item>

      </v-list>
    </v-navigation-drawer>
</v-container>
</template>

<script>
export default {
  name: 'Header',
  
  data: () => ({
    drawer: false,
    items: [
      { title: 'View Meetups', icon: 'mdi-account-group', link: '/meetups' },
      { title: 'Organize Meetup', icon: 'mdi-map-marker', link: '/meetup' },
      { title: 'Profile', icon: 'mdi-account', link: '/profile' },
      { title: 'Sign in', icon: 'mdi-face', link: '/signin' },
      { title: 'Sign up', icon: 'mdi-lock-open', link: '/signup' },
    ],
  }),
};
</script>

<style scoped>

    router-link{
        color: white;
        text-decoration: none;
        cursor: pointer;  
    }

    v-btn.navButton{
      
      background-color: red;
    }
    .v-btn:hover:before{
      background-color: red;
    }

</style>