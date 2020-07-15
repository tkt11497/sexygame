<template>
 <v-container class="pa-0 ma-0" fluid>
<v-row class="pa-0 ma-0" style="height:100vh;">
    <v-col cols="7" class="pa-0">
        <div class="playTable"> 

        </div>
       
        <v-tabs
        background-color="rgba(0, 0, 0, 1)"
        class="elevation-2"
        dark
        centered
        grow 
        height="5vh"
      >
        <v-tabs-slider></v-tabs-slider>
  
        <v-tab
          :href="`#tab-1`"
        >
          Baccarat
        </v-tab>
        <v-tab
          :href="`#tab-2`"
        >
          No Commission
        </v-tab>
        <v-tab
          :href="`#tab-3`"
        >
          Cow Cow
        </v-tab>
  
        <v-tab-item
          :value="'tab-' + 1"
        >
         <v-card
            flat
            tile
            height="30vh"
          >
           <div class="playArea">
             <v-row style="height:55%;width:100%; margin:0">
               <v-col tile cols="4" class="playArea-tile" align="center">
                 <h1> Player</h1>
                  <h2>1:1</h2>
               </v-col>
               <v-col tile cols="4" class="playArea-tile pa-0" align="center">
                <div class="tie tie1">
                  <h2> Tie</h2>
                  <h2>8:1</h2>
                </div>
                <div  class="tie">
                  <h2> Lucky Six</h2>
                  <h2> 12:1 / 20:1</h2>
                </div>
               </v-col>
               <v-col tile cols="4" class="playArea-tile banker" align="center">
                 <h1> Banker</h1>
                  <h2>0.95:1</h2>
               </v-col>
             </v-row>
             <v-row style="height:45%;width:100%; margin:0">
               <v-col tile cols="3" class="playArea-tile1" align="center">
                  <h1>Player Pair</h1>
                  <h2>11:1</h2>
               </v-col>
               <v-col tile cols="3" class="playArea-tile1" align="center">
                  <h1>Player Natural</h1>
                  <h2>7:2</h2>
               </v-col>
               <v-col tile cols="3" class="playArea-tile1 banker" align="center">
                  <h1>Banker Natural</h1>
                  <h2>7:2</h2>
               </v-col>
               <v-col tile cols="3" class="playArea-tile1 banker" align="center">
                  <h1>Banker Pair</h1>
                  <h2>11:1</h2>
               </v-col>
             </v-row>
           </div>
         </v-card>
         
        </v-tab-item>
           <v-tab-item
          :value="'tab-' + 2"
        >
          <v-card
            flat
            tile
            height="30vh"
          >
           <div class="playArea">
               <h1> 2</h1>
           </div>
          </v-card>
        </v-tab-item>
           <v-tab-item
          :value="'tab-' + 3"
        >
          <v-card
            flat
            tile
            height="30vh"
          >
           <div class="playArea">
               3
           </div>
          </v-card>
        </v-tab-item>
      </v-tabs>
       
          <div 
        style="height:4vh ;background-color:#023016"
        class="d-flex justify-center align-center white--text"
        >
            Total BetAmount : 0.0
        </div>
        <div class="selectCoin">
          
        </div>
    </v-col>
    <v-col cols="4">
      <v-tabs
        background-color="rgba(0, 0, 0, 1)"
        class="elevation-2"
        dark
        centered
        grow 
        height="5vh"
      >
        <v-tabs-slider></v-tabs-slider>
  
        <v-tab
          :href="`#tab-1`"
        >
          Table Info
        </v-tab>
        <v-tab
          :href="`#tab-2`"
        >
          Video
        </v-tab>
        <v-tab
          :href="`#tab-3`"
        >
          Cards
        </v-tab>
  
        <v-tab-item
          :value="'tab-' + 1"
        >
         <v-card
            flat
            tile
            height="31vh"
          >
          <v-row style="height:80%;width:100%; margin:0;background-color:red; ">
          <v-col style="width:50%; background-color:red; padding:0 ">
            <v-row style="background-color:purple;margin:0;" dense>
             <v-col cols="6"> Banker 65</v-col>  
             <v-col cols="6">2242532/1213</v-col>
            </v-row>
          </v-col>
          <v-col style="width:50%; background-color:blue;padding:0">
          </v-col>
          </v-row>
         </v-card>
         
        </v-tab-item>
           <v-tab-item
          :value="'tab-' + 2"
        >
          <v-card
            flat
            tile
            height="31vh"
          >
           <div class="playArea">
               <h1> 2</h1>
           </div>
          </v-card>
        </v-tab-item>
           <v-tab-item
          :value="'tab-' + 3"
        >
          <v-card
            flat
            tile
            height="31vh"
          >
           <div class="playArea">
               3
           </div>
          </v-card>
        </v-tab-item>
      </v-tabs>
    </v-col>
    <v-col cols="1">
        <h1>HHIII </h1>
    </v-col>
</v-row>
    
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
    .playTable{
        background-image: url("~assets/images/table.png");
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 50%;
        position: relative;
    }
    .playArea-tile{
        border:1px solid rgba(255,255,255, 0.3);
        color:#3470A9;
        font-size:1.2vw ;
    }
     .playArea-tile1{
        border:1px solid rgba(255,255,255, 0.3);
        color:#3470A9;
        font-size:0.7vw ;
    }
    .banker{
      color:red
    }
    .tie{
      height:50%;
      width:100%; 
      margin:0;
      color:#0C930A;
       font-size:0.9vw ;
    }
    .tie1{
      border-bottom: 1px solid  rgba(255,255,255, 0.3);
    }
    .playArea{
        background-color:rgb(3, 62, 29);
        width:100%;
        height:100%
    }
    .selectCoin{
        width: 100%;
        height: 11vh;
        background-color: brown;
    }
</style>
