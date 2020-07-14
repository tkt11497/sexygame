<template>
 <v-container class="pa-0">
<v-flex row class="pa-0">
    <v-col cols="7" class="pa-0">
        <div class="playTable"> 

        </div>
        <div class="playDiv">
        <v-tabs
        background-color="deep-purple accent-4"
        class="elevation-2"
        dark
        centered
        grow 
      >
        <v-tabs-slider></v-tabs-slider>
  
        <v-tab
          v-for="i in 3"
          :key="i"
          :href="`#tab-${i}`"
        >
          Tab {{ i }}
          <v-icon v-if="icons">mdi-phone</v-icon>
        </v-tab>
  
        <v-tab-item
          v-for="i in 3"
          :key="i"
          :value="'tab-' + i"
        >
          <v-card
            flat
            tile
            height="300px"
          >
           <div class="playArea">
           </div>
          </v-card>
        </v-tab-item>
      </v-tabs>
        <div style="height:42px ;background-color:red">

        </div>
        </div>
    </v-col>
    <v-col cols="4">
        <h1>HHIII </h1>
    </v-col>
    <v-col cols="1">
        <h1>HHIII </h1>
    </v-col>
</v-flex>
    
 </v-container>
</template>

<script>
export default {
  data () {
    return {
    
      
            }
            }
}
</script>
<style scoped>
    .container{
        padding: 0px;
    }
    .playTable{
        background-image: url("~assets/images/table.png");
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 450px;
        position: relative;
    }
    .playDiv{
        width: 100%;
        height: 390px;
        background-color: black;
    }
</style>
