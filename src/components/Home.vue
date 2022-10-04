<template>
    
  <v-container>
      <v-row>
        <v-col lg="6" md="6" sm="12" cols="6"  offset-lg="0"  offset-md="3" offset-sm="0">
          <v-btn router to="/meetups" x-large outline block color="primary" style="text-decoration: none">
            Explore Meetups
          </v-btn>
        </v-col>
        <v-col lg="6" md="6" sm="12" cols="6" offset-cols="3" offset-lg="0" offset-md="3" offset-sm="0">
          <v-btn  router to="/meetup"  x-large outline block color="primary" style="text-decoration: none"> 
            Create Meetup
          </v-btn>
        </v-col>
      </v-row>
      <v-row >
        <v-col lg="9" md="12" cols="12">
          <v-carousel cycle hide-delimiters :show-arrows="false" height="auto">
              <v-carousel-item 
              v-for="(item,i) in meetups" :key="i"
                  :src="item.src"
                  style="object-fit: fill"
                  >
              </v-carousel-item>
          </v-carousel>
        </v-col>
        <v-col lg="3" md="12" cols="12">
          <v-card
           height="100%" 
            margin="none"
            class="mx-auto"
            width="100%"
          >
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-row>
              <v-col lg="12" md="6" class="d-none d-md-flex">
                <v-carousel cycle hide-delimiters :show-arrows="false" height="auto">
                  <v-carousel-item 
                  v-for="(item,i) in meetups" :key="i"
                      :src="item.src"
                      style="object-fit: fill"
                      >
                  </v-carousel-item>
              </v-carousel>
              </v-col>
              <v-col lg="12" md="6" cols="12" class="py-0">
                <v-card-title>Neki naslov</v-card-title>
                <v-card-text class="pb-3" vertical-align="center">
                  <v-row
                    
                    align="center"
                    class="mx-0"
                  >
                    <v-rating
                      :value="4.5"
                      color="amber"
                      dense
                      half-increments
                      readonly
                      size="14"
                    ></v-rating>

                    <div class="grey--text ms-4">
                      4.5 (413)
                    </div>
                  </v-row>

                  <div class="my-4 text-subtitle-1">
                    $ • Neka glupost
                  </div>

                  <div>Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                    Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                    when an unknown printer took a galley of type and scrambled it to make a type specimen book. </div>
                </v-card-text>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
    
  </v-container>
  
</template>

<script>
export default {
    name: 'Home',
    data () {
      return {
        meetups: [
          {
            src: 'https://www.travelandleisure.com/thmb/gPCyzXAnVMK116tKpy03OWXtEZI=/2000x0/filters:no_upscale():max_bytes(150000):strip_icc():gifv():format(webp)/new-york-city-evening-NYCTG0221-52492d6ccab44f328a1c89f41ac02aea.jpg',
          },
          {
            src: 'https://media.cntraveler.com/photos/5d8cf7d5db6acf000833e6cc/master/pass/Eiffel-Tower_GettyImages-1060266626.jpg',
          },
          {
            src: 'https://a.cdn-hotels.com/gdcs/production29/d1375/234f7170-c9f4-4cee-a372-1a198e388483.jpg'
          }
        ],
      }
    },
}
</script>

<style scoped>

    p{
        text-align: center;
        padding-top: 100px;
    }



</style>