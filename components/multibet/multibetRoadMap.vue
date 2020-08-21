<template>

  <v-flex md6 mt-1 >
  <!-- Start card -->
   <v-card min-height="258" class="mt-2 ml-2 mr-1">
     <div class="dashboard-card">
         <v-layout>
             <v-flex mt-3 mb-2 ml-5>
               <span class="black--text">Seri {{ project.seri}}</span>
             </v-flex>

             <v-flex mt-3 mb-2>
                <span class="red--text">庄</span>
                <span class="black--text">{{project.bb}}</span>
             </v-flex>

             <v-flex mt-3 mb-2>
                  <span class="blue--text">圓</span>
                  <span class="black--text">{{project.pp}}</span>
             </v-flex>

             <v-flex mt-3 mb-2>
               <div class="black--text">
                 <span class="green--text">和</span>
                 {{project.tt}}
               </div>
             </v-flex>

             <v-spacer></v-spacer><v-spacer></v-spacer>
             <v-flex mt-1 mb-1>
               <v-btn @click="favoriteshow=true" icon medium color="#787878"><v-icon>favorite</v-icon></v-btn>
             </v-flex>

             <v-flex mt-1 mb-1>
               <v-btn icon medium color="#c3a475">
                   <v-icon>switch_video</v-icon>
               </v-btn>
             </v-flex>

             <v-flex>
                   <div class=" d-flex justify-center align-center black--text" style="background:#c6c6c9; height:44px;">
                     <div> {{project.status}} </div>
                   </div>
             </v-flex>
           </v-layout>
        </div>

           <v-img
           height="100%"
           src="/icon/珠盤路單(大).png"
           >

           </v-img>

         <v-tabs class="tabform"
         v-model="tab"
         background-color="#404040 accent-4"
         active-class="orange lighten-4 black--text"
         height="25"
         centered
         dark
         icons-and-text
         fixed-tabs
         >
       <v-tabs-slider></v-tabs-slider>

       <v-tab href="#tab-1">
         Baccarat
       </v-tab>

       <v-tab href="#tab-2">
         No Commission
       </v-tab>

       <v-tab href="#tab-3">
         Cow Cow ?
       </v-tab>

       <v-tab-item :value="'tab-' + 1">
         <v-card
            flat
            tile

          >
           <div class="playArea">
             <v-row style="margin:0;">
               <v-col tile cols="2" class="playArea-tile" align="center">
                 <h3>Player</h3>
               </v-col>
               <v-col tile cols="2" class="playArea-tile tile" align="center">
                 <h3>Tie</h3>
               </v-col>
               <v-col tile cols="2" class="playArea-tile banker" align="center">
                 <h3>Banker</h3>
               </v-col>
               <v-col tile cols="2" class="playArea-tile" align="center">
                  <h3>P.Pair</h3>
               </v-col>
               <v-col tile cols="2" class="playArea-tile tile" align="center">
                  <h3>Lucky Six</h3>
               </v-col>
               <v-col tile cols="2" class="playArea-tile banker" align="center">
                  <h3>B.Pair</h3>
               </v-col>

             </v-row>
           </div>
         </v-card>
       </v-tab-item>

       <v-tab-item :value="'tab-' + 2">
         <v-card
            flat
            tile

          >
          <div class="playArea">
            <v-row style="margin:0;">
              <v-col tile cols="2" class="playArea-tile" align="center">
                <h3>Player</h3>
              </v-col>
              <v-col tile cols="2" class="playArea-tile tile" align="center">
                <h3> Tie</h3>
              </v-col>
              <v-col tile cols="2" class="playArea-tile banker" align="center">
                <h3> Banker</h3>
              </v-col>
              <v-col tile cols="2" class="playArea-tile" align="center">
                 <h3>P.Pair</h3>
              </v-col>
              <v-col tile cols="2" class="playArea-tile tile" align="center">
                 <h3>Lucky Six</h3>
              </v-col>
              <v-col tile cols="2" class="playArea-tile banker" align="center">
                 <h3>B.Pair</h3>
              </v-col>

            </v-row>
          </div>
         </v-card>
       </v-tab-item>

       <v-tab-item :value="'tab-' + 3">
         <v-card
            flat
            tile

          >
           <div class="playArea">
             <v-row style="margin:0;">
               <v-col tile cols="4" class="playArea-tile-last" align="center" >
                 <h2>Player</h2>
               </v-col>
               <v-col tile cols="4" class="playArea-tile-last tile" align="center">
                 <h2> Tie</h2>
               </v-col>
               <v-col tile cols="4" class="playArea-tile-last banker" align="center">
                 <h2> Banker</h2>
               </v-col>
             </v-row>
           </div>
         </v-card>
       </v-tab-item>
   </v-tabs>
</v-card>
<!-- End card -->
</v-flex>
</template>

<script>
  export default {
    props: ['project'],
    favoriteshow:false,
    data(){
      return{
        tab:null
      }
    }
  }
</script>

<style scoped>

.playArea-tile{
    border:1px solid rgba(255,255,255, 0.3);
    color:#3470A9;
    height: 64px;
    }

.playArea{
    background-color:rgb(3, 62, 29);
    height:64px;
    }

.playArea-tile-last{
    border:1px solid rgba(255,255,255, 0.3);
    color:#3470A9;
    height: 64px;
    }

.banker{
    color:red
    }

.tie{
    color:#0C930A;
    }

.tile{
    color:green
}

</style>
