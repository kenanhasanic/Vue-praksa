<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="6" md="12" lg="4" v-for="(meetup, index2) in meetups" :key="index2">
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
              <v-col lg="12" md="6" sm="12"  cols="12">
                <v-img height="100%" width="100%"
                  :src="meetup.src"
                ></v-img>
              </v-col>
              <v-col lg="12" md="6" sm="12" cols="12" class="py-0">

                <v-card-title>Neki naslov</v-card-title>

                <v-card-text class="pb-3" vertical-align="center">
                  

                  <div>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. </div>
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
  name: 'Meetups',
  data() {
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
          },
        
          {
            src: 'https://www.travelandleisure.com/thmb/gPCyzXAnVMK116tKpy03OWXtEZI=/2000x0/filters:no_upscale():max_bytes(150000):strip_icc():gifv():format(webp)/new-york-city-evening-NYCTG0221-52492d6ccab44f328a1c89f41ac02aea.jpg',
          },
          {
            src: 'https://media.cntraveler.com/photos/5d8cf7d5db6acf000833e6cc/master/pass/Eiffel-Tower_GettyImages-1060266626.jpg',
          },
          {
            src: 'https://a.cdn-hotels.com/gdcs/production29/d1375/234f7170-c9f4-4cee-a372-1a198e388483.jpg'
          },
        
        
      ]
    }
    
  }
  // ,
  // methods: {
  //   chunkedItems() {
  //     var arr = meetups
  //     var res = [];
  //     while (arr.length) {
  //       res.push(arr.splice(0, n));
  //     }
  //     console.log(res)
  //     return res;
  //   },
  // },
  // created() {
  //   this.meetups = chunkedItems()
  // }
}
</script>

<style scoped>
    p{
        text-align: center;
        padding-top: 100px;
    }
</style>