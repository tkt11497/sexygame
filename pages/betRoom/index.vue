<template>
 <v-container class="pa-0 ma-0" fluid>
<v-row class="pa-0" style="height:100vh;" no-gutters>
    <v-col class="pa-0" style="width:50% ;max-width: 50%">
        <div class="playTable"> 

        </div>
       
        <v-tabs
        background-color="rgba(0, 0, 0, 0.7)"
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
    <v-col cols="4" class="pa-0">
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
            height="32vh" 
            dark
          >
          <v-row style="height:80%;width:100%; margin:0;" class="table-info">
          <v-col style="width:50%; padding:0;border-right:1px solid white ">
            <v-row style="margin:0;" dense>
             <v-col cols="6" class="banker"> Banker 65%</v-col>  
             <v-col cols="6">2242532/1213</v-col>
              <v-progress-linear
                  v-model="progress"
                  color="red"
                ></v-progress-linear>
            </v-row>

             <v-row style="margin:0;" dense>
             <v-col cols="6" class="player"> Player 41%</v-col>  
             <v-col cols="6">2242532/1213</v-col>
              <v-progress-linear
                  v-model="progress"
                  color="blue"
                ></v-progress-linear>
            </v-row>

             <v-row style="margin:0;" dense>
             <v-col cols="6" class="tie-text"> Tie 1%</v-col>  
             <v-col cols="6">2242532/1213</v-col>
              <v-progress-linear
                  v-model="progress"
                  color="green"
                ></v-progress-linear>
            </v-row>
             <v-row style="margin:0;" dense>
             <v-col cols="6" class="banker"> Banker Pair</v-col>  
             <v-col cols="6">2242532/1213</v-col>
            </v-row>
             <v-row style="margin:0;" dense>
             <v-col cols="6" class="player"> Player Pair</v-col>  
             <v-col cols="6">2242532/1213</v-col>
            </v-row>
             <v-row style="margin:0;" dense>
             <v-col cols="6" class="banker"> Banker Natural</v-col>  
             <v-col cols="6">2242532/1213</v-col>
            </v-row>
             <v-row style="margin:0;" dense>
             <v-col cols="6" class="player"> Player Natural</v-col>  
             <v-col cols="6">2242532/1213</v-col>
            </v-row>
          </v-col>
          <v-col style="width:50%; ;padding:0">
              <v-row style="margin:0;" dense>
             <v-col cols="6" > Table</v-col>  
             <v-col cols="6">C01</v-col>
            </v-row>
              <v-row style="margin:0;" dense>
             <v-col cols="6" > Dealer</v-col>  
             <v-col cols="6">Monkey Dog</v-col>
            </v-row>
              <v-row style="margin:0;" dense>
             <v-col cols="6" > Round</v-col>  
             <v-col cols="6">3-25</v-col>
            </v-row>
              <v-row style="margin:0;" dense>
             <v-col cols="6" > ID</v-col>  
             <v-col cols="6">1291200211</v-col>
            </v-row>
              <v-row style="margin:0;" dense>
             <v-col cols="6" > Table Limit</v-col>  
             <v-col cols="6">20000</v-col>
            </v-row>
              <v-row style="margin:0;" dense>
             <v-col cols="6" > Max. Limit</v-col>  
             <v-col cols="6">5000</v-col>
            </v-row>
              <v-row style="margin:0;" dense>
             <v-col cols="6" > Min. Limit</v-col>  
             <v-col cols="6">100</v-col>
            </v-row>
          </v-col>
          </v-row>

           <v-row style="height:20%;width:100%; margin:0; " class="table-info">
             <v-col cols="2" class="text-center">
               <span>Banker</span><br>
               <span>5000</span>
             </v-col>
             <v-col  cols="2" class="text-center">
               <span>Player</span><br>
               <span>5000</span>
             </v-col >
             <v-col  cols="2" class="text-center">
               <span>Tie</span><br>
               <span>5000</span>
             </v-col>
             <v-col  cols="2" class="text-center">
               <span>Pair</span><br>
               <span>500</span>
             </v-col>
             <v-col  cols="2" class="text-center">
               <span>Natural</span><br>
               <span>5000</span>
             </v-col>
             <v-col  cols="2" class="text-center d-flex align-center justify-center" >
            <v-btn x-small>
               change
            </v-btn>
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
  <div style="height:13% ;background-color:black" >
     <v-row style="height:50%;width:100%; margin:0;" >
       <div style="width:12.5%;" class="d-flex justify-center align-center">
         <v-card height="80%" width="80%"  color="secondary" dark 
         class="d-flex justify-center align-center room-list">C01</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">C02</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">C03</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">C06</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">C07</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">P01</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">P02</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">P03</v-card>
       </div>
     </v-row>
      <v-row style="height:50%;width:100%; margin:0;">
       <div style="width:12.5%;" class="d-flex justify-center align-center">
         <v-card height="80%" width="80%"  color="secondary" dark 
         class="d-flex justify-center align-center room-list"
         @click="window=2">C01</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">C02</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">C03</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">C06</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list">C07</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list"
          @click="window=1">P01</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card height="80%" width="80%"  color="secondary" dark 
          class="d-flex justify-center align-center room-list"
          @click="window=2">P02</v-card>
       </div>
        <div style="width:12.5%;" class="d-flex justify-center align-center">
          <v-card  height="80%" width="80%" color="secondary" dark 
          class="d-flex justify-center align-center room-list"
          @click="window=3">P03</v-card>
       </div>
     </v-row>
      
  </div>
    <v-window v-model="window">
        <v-window-item :value="1">
           <div class="text-center" style="height:46vh; width:100%;background-color:black">
            <div style="width:100%; height:30%">
             <previewTable :row="6" :column="36"/>
            </div>
            <v-divider/>
            <div style="width:100%; height:10%">
              <previewTable :row="3" :column="36"/>
            </div>
            <v-divider/>
            <v-row style="width:100%; height:10%" no-gutters>
              <div style="width:49.7%; height:100%; ">
               <previewTable :row="3" :column="16"/>
              </div>
              <v-divider vertical/>
              <div style="width:50%; height:100%">
                 <previewTable :row="3" :column="16"/>
              </div>
            </v-row>
            <v-divider/>
            <div style="width:100%; height:40%">
              <previewTable :row="6" :column="18"/>
            </div>
            <v-row no-gutters style="width:100%; height:10%">
            <div class="d-flex align-center justify-left room-list" style="width:50%; height:100%; background-color:black">
              <span class="font-weight-bold red--text ml-1">B</span>
              <span class="font-weight-bold white--text ml-1">13</span>
              <span class="font-weight-bold blue--text ml-1">P</span>
              <span class="font-weight-bold white--text ml-1">123</span>
              <span class="font-weight-bold green--text ml-1">T</span>
              <span class="font-weight-bold white--text ml-1">13</span>
              <span class="font-weight-bold red--text ml-1">BP</span>
              <span class="font-weight-bold white--text ml-1">13</span>
              <span class="font-weight-bold blue--text ml-1">PP</span>
              <span class="font-weight-bold white--text ml-1">133</span>
            </div>
             <div class="d-flex align-center justify-left room-list" style="width:50%; height:100%; background-color:black">
                <v-btn x-small color="red" class="ml-1"> <span class="white--text"> Ask B.</span></v-btn>
                <v-progress-circular 
                :value="100"  
                width="3" 
                color="blue"
                class="ml-1" 
                size="15"
                ></v-progress-circular>
                <v-avatar color="blue" class="ml-1" size="15">
                  
                </v-avatar>
                <span class="font-weight-bold red--text ml-1 mr-5  ">/</span>
                 <v-btn x-small color="blue" class="ml-1"><span class="white--text"> Ask P.</span></v-btn>
                <v-progress-circular 
                :value="100"  
                width="3" 
                color="red"
                class="ml-1" 
                size="15"
                ></v-progress-circular>
                <v-avatar color="red" class="ml-1" size="15">
                  
                </v-avatar>
                <span class="font-weight-bold blue--text ml-1">/</span>
             </div>
            </v-row>
          </div>
        </v-window-item>
  
        <v-window-item :value="2">
         <div class="pa-4 text-center" style="height:100%; width:100%;background-color:black">
            <v-text-field
              label="Password"
              type="password"
            ></v-text-field>
            <v-text-field
              label="Confirm Password"
              type="password"
            ></v-text-field>
            <span class="caption grey--text text--darken-1">
              Please enter a password for your account
            </span>
          </div>
        </v-window-item>
  
        <v-window-item :value="3">
          <div class="pa-4 text-center" style="height:100%; width:100%;background-color:black">
            <v-img
              class="mb-4"
              contain
              height="128"
              src="https://cdn.vuetifyjs.com/images/logos/v.svg"
            ></v-img>
            <h3 class="title font-weight-light mb-2">Welcome to Vuetify</h3>
            <span class="caption grey--text">Thanks for signing up!</span>
          </div>
        </v-window-item>
      </v-window> 
    
    
    
    </v-col>
    <v-col cols="2">
      
         <v-card height="50vh" >

          <v-expansion-panels flat> 
            <v-expansion-panel>
              <v-expansion-panel-header color="black">
                <span class="white--text">Switch Table</span>
                  <template v-slot:actions>
                  <v-icon color="white">clear_all</v-icon>
                </template>
              </v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-row class="d-flex justify-center align-center ma-0 pa-0">
                 <v-checkbox label="Checkbox 1"
                  ></v-checkbox>
                  <v-checkbox label="Checkbox 1"
                  ></v-checkbox>
                </v-row>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
          <v-divider></v-divider>
          <v-card-text style="height: 85%;" class="scroll pa-0 ma-0">
                  <v-card height="150px" class="mb-2" color="blue">
                    <v-system-bar
                        color="black"
                        dark
                        class="ma-0 pa-0"
                      >
                      <span class="room-list ml-1 white--text">Baccarat C02</span>
                            <v-spacer></v-spacer>

                            <div class="d-flex justify-center align-center ma-0 pa-0"
                            style="width:30%;height:100%;background-color:#196260">
                              <span>20</span>
                            </div>

                          </v-system-bar>
                          <previewTable :row="7" :column="16"/>
                  </v-card>
                  <v-card height="150px" class="mb-2" color="blue">
                    <v-system-bar
                        color="black"
                        dark
                        class="ma-0 pa-0"
                      >
                      <span class="room-list ml-1 white--text">Baccarat C02</span>
                            <v-spacer></v-spacer>

                            <div class="d-flex justify-center align-center ma-0 pa-0"
                            style="width:30%;height:100%;background-color:#196260">
                              <span>20</span>
                            </div>

                          </v-system-bar>
                          <previewTable :row="7" :column="16"/>
                  </v-card>
                  <v-card height="150px" class="mb-2" color="blue">
                    <v-system-bar
                        color="black"
                        dark
                        class="ma-0 pa-0"
                      >
                      <span class="room-list ml-1 white--text">Baccarat C02</span>
                            <v-spacer></v-spacer>

                            <div class="d-flex justify-center align-center ma-0 pa-0"
                            style="width:30%;height:100%;background-color:#196260">
                              <span>20</span>
                            </div>
                          </v-system-bar>
                        <previewTable :row="7" :column="16"/>
                  </v-card>
                  <v-card height="150px" class="mb-2" color="blue">
                    <v-system-bar
                        color="black"
                        dark
                        class="ma-0 pa-0"
                      >
                      <span class="room-list ml-1 white--text">Baccarat C02</span>
                            <v-spacer></v-spacer>

                            <div class="d-flex justify-center align-center ma-0 pa-0"
                            style="width:30%;height:100%;background-color:#196260">
                              <span>20</span>
                            </div>

                          </v-system-bar>

                          <previewTable :row="7" :column="16"/>
                  </v-card>
          </v-card-text>
        </v-card>

         <v-card height="46vh" >
           <v-system-bar
                    color="black"
                    dark
                    class="ma-0 pa-0" 
                    height="35"
                  >
                  <span class="room-list ml-5 white--text">Good Road</span>
                        <v-spacer></v-spacer>

                        <v-icon color="white">mdi-menu-down</v-icon>
            </v-system-bar>
          <v-divider></v-divider>
          <v-card-text style="height: 85%;" class="scroll pa-0 ma-0">
                    <v-card height="150px" class="mb-2" color="blue">
                    <v-system-bar
                        color="black"
                        dark
                        class="ma-0 pa-0"
                      >
                      <span class="room-list ml-1 white--text">Baccarat C02</span>
                            <v-spacer></v-spacer>

                            <div class="d-flex justify-center align-center ma-0 pa-0"
                            style="width:30%;height:100%;background-color:#196260">
                              <span>20</span>
                            </div>

                          </v-system-bar>
                          <previewTable :row="7" :column="16"/>
                  </v-card>
                  <v-card height="150px" class="mb-2" color="blue">
                    <v-system-bar
                        color="black"
                        dark
                        class="ma-0 pa-0"
                      >
                      <span class="room-list ml-1 white--text">Baccarat C02</span>
                            <v-spacer></v-spacer>

                            <div class="d-flex justify-center align-center ma-0 pa-0"
                            style="width:30%;height:100%;background-color:#196260">
                              <span>20</span>
                            </div>

                          </v-system-bar>
                          <previewTable :row="7" :column="16"/>
                  </v-card>
                  <v-card height="150px" class="mb-2" color="blue">
                    <v-system-bar
                        color="black"
                        dark
                        class="ma-0 pa-0"
                      >
                      <span class="room-list ml-1 white--text">Baccarat C02</span>
                            <v-spacer></v-spacer>

                            <div class="d-flex justify-center align-center ma-0 pa-0"
                            style="width:30%;height:100%;background-color:#196260">
                              <span>20</span>
                            </div>
                          </v-system-bar>
                        <previewTable :row="7" :column="16"/>
                  </v-card>
                  <v-card height="150px" class="mb-2" color="blue">
                    <v-system-bar
                        color="black"
                        dark
                        class="ma-0 pa-0"
                      >
                      <span class="room-list ml-1 white--text">Baccarat C02</span>
                            <v-spacer></v-spacer>

                            <div class="d-flex justify-center align-center ma-0 pa-0"
                            style="width:30%;height:100%;background-color:#196260">
                              <span>20</span>
                            </div>

                          </v-system-bar>

                          <previewTable :row="7" :column="16"/>
                  </v-card>
          </v-card-text>
        </v-card>
        
     
    </v-col>
</v-row>
    
 </v-container>
</template>

<script>
import previewTable from '@/components/previewTable';
export default {
  components:{
        previewTable
    },
  data () {
    return {
      progress:50,
      window:1,
     
            }
            }
}
</script>
<style scoped>
 .scroll {
      overflow-y: auto;
    }
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
    .player{
      color:#3470A9
    }
    .banker{
      color:red
    }
    .tie-text{
      color:#0C930A;
    }
    .tie{
      height:50%;
      width:100%; 
      margin:0;
      color:#0C930A;
       font-size:0.75vw ;
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
    }
    .table-info{
      font-size: 0.8vw;
    }
    .room-list{
        font-size: 0.8vw;
    }
    
</style>
