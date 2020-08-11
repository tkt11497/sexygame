<template>
 <v-container class="pa-0 ml-1" fluid style="background-color:black">
<v-row class="pa-0" style="height:100vh;" no-gutters>
    <v-col class="pa-0" cols="7">
        <div class="playTable"> 
           <v-btn class="mx-2"  dark small color="#4F3C2B" style="position:absolute;bottom:1%;left:0" link to="/betRoom/betRoom2">
              <v-icon dark>picture_in_picture</v-icon>
            </v-btn>
            <v-btn class="mx-2"  dark small color="#4F3C2B" style="position:absolute;bottom:10%;right:0">
              <v-icon dark>switch_video</v-icon>
            </v-btn>
            <v-btn class="mx-2"  dark small color="#4F3C2B" style="position:absolute;bottom:1%;right:0">
              <v-icon dark>fullscreen</v-icon>
            </v-btn>
            <div class="room-title d-flex justify-center align-center white--text">
                    Baccrart C01
            </div>
              <v-avatar 
                    color="rgba(0,0,0,0.5)" 
                    size="130" 
                    class="gameCountDown" 
                    v-show="true">
                        <v-progress-circular
                        :value="70"
                        color="red" 
                        size="100"
                        >
                    <span> 60</span>
                    </v-progress-circular>
                </v-avatar>
        </div>
       
        <v-tabs
        background-color="#404040"
        class="elevation-2"
        centered
        grow 
        dark
        height="4vh" 
        hide-slider 
        active-class="tabActive black--text"
      >
        <!-- <v-tabs-slider></v-tabs-slider> -->
  
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
           <div class="playArea" >
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
                  <h2>1:1</h2>
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
          :value="'tab-' + 3"
        >
          <v-card
            flat
            tile
            height="30vh"
          >
           <div class="playArea">
              <v-row style="height:100%;width:100%; margin:0">
                  <v-col tile cols="4" class="playArea-tile" align="center">
                    <h1> Player</h1>
                      <h2>1:1</h2>
                  </v-col>
                  <v-col tile cols="4" class="playArea-tile" align="center">
                  
                      <h2> Tie</h2>
                      <h2>8:1</h2>
                    
                  </v-col>
                  <v-col tile cols="4" class="playArea-tile banker" align="center">
                    <h1> Banker</h1>
                      <h2>1:1</h2>
                  </v-col>
             </v-row>
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
        <div class="selectCoin d-flex align-center white--text pa-2" >
                              
                            <v-menu
                              offset-y
                              top 
                              :close-on-content-click="false"
                              v-model="coinMenu"
                              :nudge-width="450"
                              :max-width="450" 
                              dark
                              >
                                  <template v-slot:activator="{ on, attrs }">
                                                  <div class="text-center mt-1 mx-2"
                                                  style="width:2.7vw;
                                                   height:2.6vw;
                                                    background-image:url('/icon/七人座自定UI.png');
                                                    background-repeat: no-repeat;
                                                    background-position: center;
                                                    background-size: 100% 100%"
                                                  v-bind="attrs"
                                                    v-on="on" 
                                                    @click="openCoinSelect">
                                                      

                                                  </div>
                                  </template>
                                  <v-card color='rgba(0, 0, 0, 0.7)' elevation="20">
                                    <v-card-title>
                                      <v-row no-gutters justify="center"> Please Select
                                        
                                       
                                      </v-row>
                                      </v-card-title>
                                      <v-row no-gutters justify="center"> 
                                          <v-img
                                                v-for="(coin,n) in coinList" :key="n"
                                                class="text-center ma-2"
                                                max-width="3.7vw" 
                                                max-height="2.6vw"
                                                :src="'/coin/'+coin"
                                              >
                                                <v-checkbox v-model="selectedCoin"
                                                 :value="coin" 
                                                 color="#009167"
                                                 :disabled="disableCoinSelect?selectedCoin.includes(coin)?false:true:false"
                                                 ></v-checkbox>
                                              </v-img>
                                            
                                      </v-row>
                                    <v-card-actions >
                                    <v-row justify="center">
                                      <!-- <v-btn small class="mx-2" fab dark color="#4f3c2b" @click="cancelCoinSelect"> -->
                                        
                                        <v-img src="/icon/萬用選擇UI.png" 
                                        @click="cancelCoinSelect" 
                                        class="ma-2"
                                        max-width="2.5vw" 
                                        max-height="2.5vw"></v-img>
                                        
                                      <!-- </v-btn> -->
                                      <v-img src="/icon/萬用取消UI.png" 
                                        @click="changeShowing"
                                        class="ma-2"
                                        max-width="2.5vw" 
                                        max-height="2.5vw"></v-img>
                                        
                                    </v-row>
                                    </v-card-actions>
                                  </v-card>
                              
                            </v-menu>
                            <div :style="{
                                        'background-image': 'url(\'/coin/'+ `${betCoin==coin?'籌碼發光.png':''}` + '\')',
                                        'background-repeat': 'no-repeat',
                                        'background-position': 'center',
                                        'background-size': '100% 100%',
                                        width:'4.9vw',height:'3.9vw'}" 
                                  @click="betCoin=coin"
                                  v-for="(coin,n) in showingCoin" 
                                  :key="n"
                                  class="pa-3" 
                                  >
                            <v-img 
                                  max-width="3.7vw" 
                                  max-height="2.6vw" 
                                  :src="'/coin/'+coin" 
                                  
                                  >
                            </v-img>
                            </div>
                              <div class="text-center mt-1 ml-2"
                                                    style="width:2.7vw;
                                                    height:2.6vw;
                                                      background-image:url('/icon/單人雙倍ui.png');
                                                      background-repeat: no-repeat;
                                                      background-position: center;
                                                      background-size: 100% 100%">
                                                        

                                </div>
                           
      
        </div>
    </v-col>
    <v-col cols="5" class="pa-0">
      <v-tabs
        background-color="rgba(0, 0, 0, 1)"
        class="elevation-2"
        dark
        centered
        grow 
        height="5vh" 
        hide-slider 
        active-class="tabActive black--text" 
      >
        
  
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
            color="#2E2E2E"
          >
          <v-row style="height:77%;width:100%; margin:0;" class="table-info">
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
                <v-col style="width:50%; ;padding:0;color:#E7CAA0">
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

           <v-row style="height:19%;width:100%; margin:0;background-color:black "  class="table-info">
             <v-col cols="2" class="text-center">
               <span style="color:#E7CAA0">Banker</span><br>
               <span>{{ changenumbers[betLimit].bet_limit }}</span>
             </v-col>
             <v-col  cols="2" class="text-center">
               <span style="color:#E7CAA0">Player</span><br>
               <span>{{ changenumbers[betLimit].bet_limit }}</span>
             </v-col >
             <v-col  cols="2" class="text-center">
               <span style="color:#E7CAA0">Tie</span><br>
               <span>{{ changenumbers[betLimit].bet_limit }}</span>
             </v-col>
             <v-col  cols="2" class="text-center">
               <span style="color:#E7CAA0">Pair</span><br>
               <span>{{ changenumbers[betLimit].bet_limit }}</span>
             </v-col>
             <v-col  cols="2" class="text-center">
               <span style="color:#E7CAA0">Natural</span><br>
               <span>{{ changenumbers[betLimit].bet_limit }}</span>
             </v-col>
             <v-col  cols="2" class="text-center d-flex align-center justify-center" >
                <v-menu
                  offset-y
                  top
                  close-on-content-click
                  :nudge-width="100"
                  left
                  :max-width="250"
                  >
                  <template v-slot:activator="{ on, attrs }">

                          <v-btn small
                          v-bind="attrs"
                            v-on="on" 
                            color="white" 
                            elevation="24">
                              <span style="color:black">change</span>
                            </v-btn>
                  </template>


                    <v-card color='rgba(0, 0, 0, 0.7)'>
                          <v-list
                          dark

                          color='rgba(0, 0, 0, 0.5)'>

                          <v-radio-group v-model="betLimit" :mandatory="false">
                            <v-radio label="10 - 1,000" value='10-1000' on-icon="done" off-icon="" ></v-radio>
                            <v-radio label="50 - 5,000" value='50-5000' on-icon="done" off-icon="" ></v-radio>
                            <v-radio label="100 - 5,000" value='100-5000' on-icon="done" off-icon=""></v-radio>
                            <v-radio label="100 - 10K" value='100-10k' on-icon="done" off-icon=""></v-radio>
                            <v-radio label="200 - 20K" value='200-20k' on-icon="done" off-icon=""></v-radio>
                          </v-radio-group>

                      </v-list>
                    </v-card>
                </v-menu>
        
             </v-col>
     
           </v-row>
            <v-row @click="exten=!exten" style="height:5%;width:100%; margin:0; background-color:#876F4D" justify="center" >
               <div style="width:100%;height:100%" class="d-flex justify-center algin-center">
              <v-icon dense x-small v-show="exten">keyboard_arrow_up</v-icon>
              <v-icon dense x-small v-show="!exten">keyboard_arrow_down</v-icon>
              
               </div>
                
            </v-row>
         </v-card>
         <v-banner dark color="black" v-model="exten" single-line transition="slide-y-transition">
           <span style="color:#E7CAA0">Lucky Six</span><br>
               <span>{{ changenumbers[betLimit].bet_limit }}</span>
            <!-- <template v-slot:actions="{ dismiss }">
              <v-btn text color="primary" @click="dismiss">Dismiss</v-btn>
              <v-btn text color="primary">Retry</v-btn>
            </template> -->

          </v-banner>
        </v-tab-item>
           <v-tab-item
          :value="'tab-' + 2"
        >
          <v-card
            flat
            tile
            height="32vh"
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
            height="32vh"
          >
          
                <div class="result-cards"> 
                    <img 
                    src="/card.png" 
                     style="width:20%; height:42%; position:absolute;left:15%;top:5%; transform: rotate(-90deg);"/>
                    <img 
                    src="/card.png" 
                     style="width:20%; height:42%; position:absolute;left:5%;bottom:18%"/>
                     <img 
                    src="/card.png" 
                     style="width:20%; height:42%; position:absolute;left:27%;bottom:18%"/>
                    <div 
                    class=" d-flex justify-center align-center"
                    style="width:42%; height:10%; position:absolute; top:85%; left:5%; background-color:blue"> 
                        <span>P 6</span>
                    </div>
                      <img 
                    src="/card.png" 
                     style="width:19%; height:42%; position:absolute;right:15%;top:5%; transform: rotate(-90deg);"/>
                    <img 
                    src="/card.png" 
                     style="width:19%; height:42%; position:absolute;right:5%;bottom:18%"/>
                     <img 
                    src="/card.png" 
                     style="width:19%; height:42%; position:absolute;right:27%;bottom:18%"/>
                    <div 
                    class=" d-flex justify-center align-center"
                    style="width:42%; height:10%; position:absolute; top:85%; right:5%; background-color:red"> 
                        <span>B 5</span>
                    </div>
                </div>
           
          </v-card>
        </v-tab-item>
      </v-tabs>
  <v-row no-gutters>
    <v-col cols="9">
      <div style="height:13vh;width:100%; background-color:#2E2E2E" >
        <v-row style="height:100%;width:100%; margin:0;" no-gutters justify="left" >
          <div style="height:50%;width:12.5%;" 
          class="d-flex justify-center align-center" 
          v-for="n in 3" :key="n">
            <v-card height="80%" width="80%"   dark 
            class="d-flex justify-center align-center room-list" 
            @click="window=n" 
            :class="{ 'windowActive': window==n }">C0{{n}}</v-card>
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
                    <span class="font-weight-bold red--text ml-1">庄</span>
                    <span class="font-weight-bold white--text ml-1">13</span>
                    <span class="font-weight-bold blue--text ml-1">圓</span>
                    <span class="font-weight-bold white--text ml-1">123</span>
                    <span class="font-weight-bold green--text ml-1">和</span>
                    <span class="font-weight-bold white--text ml-1">13</span>
                    <span class="font-weight-bold red--text ml-1">庄庄</span>
                    <span class="font-weight-bold white--text ml-1">13</span>
                    <span class="font-weight-bold blue--text ml-1">和和</span>
                    <span class="font-weight-bold white--text ml-1">133</span>
                  </div>
                  <div class="d-flex align-center justify-left room-list" style="width:50%; height:100%; background-color:black">
                      <v-btn small color="#c70000" class="ml-1"> <span class="white--text">庄問路</span></v-btn>
                      <v-img
                                          max-width="1vw"
                                          max-height="1vw"
                                          src="/icon/大紅圈.png"
                                        />
                      <v-avatar color="#c70000" class="ml-1" size="15">
                        
                      </v-avatar>
                      <span class="font-weight-bold red--text ml-1 mr-5  ">/</span>
                      <v-btn small color="#2d30b1" class="ml-1"><span class="white--text"> 閒問路</span></v-btn>
                       <v-img
                                          max-width="1vw"
                                          max-height="1vw"
                                          src="/icon/大藍圈.png"
                                        />
                      <v-avatar color="#2d30b1" class="ml-1" size="15">
                        
                      </v-avatar>
                      <span class="font-weight-bold ml-1" style="color:#2d30b1">/</span>
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
    <v-col cols="3">
      
                  <v-card height="53vh" class="my-3 mx-1 cardGradient" >
                    <v-system-bar
                        color="#AA8647"
                        dark
                        class="ma-0 pa-0"
                      >
                        <span class="room-list ml-1 black--text">Baccarat C02</span>
                            <v-spacer></v-spacer>
                            <div class="d-flex justify-center align-center ma-0 pa-0"
                            style="width:30%;height:100%;">
                             <v-btn icon small>
                              <v-icon>settings</v-icon>
                             </v-btn>
                            </div>

                    </v-system-bar>
                      <v-card
                          color="rgba(255,2555,255,0)"
                          height="8vh" 
                          class="d-flex align-center justify-space-between " 
                          v-for="n in 6" 
                          :key="n"
                        >
                         <div class="ml-1">
                               <v-avatar 
                                  color="#4C4331" 
                                  size="2vw" 
                                >
                                      <v-progress-circular
                                      :value="100"
                                      color="#F7A823" 
                                      size="30" 
                                      width="2"
                                      >
                                 
                                  </v-progress-circular>
                              </v-avatar>
                         </div> 
                         <span style="font-size:0.7vw">blahblah</span> 
                         <div style="background-color:#EAEDEA;width:3vw;height:3vw" class="ma-2">
                         </div> 
                        </v-card>
                        
                  </v-card>
                
    </v-col>
  </v-row>
    
    
    
    </v-col>
    
</v-row>
   
      <button v-show="!drawer" class="Custombutton"  style="position:absolute; top:12vh;right:0" @click="drawer=true" >
        <p class="py-5" style="writing-mode: vertical-rl;text-orientation: upright;letter-spacing:-2px;font-size:0.8vw">
          tables
        </p>
      </button>
    
    
  <tableDrawer :drawer="drawer"  @close="drawer=false"/>
 </v-container>
 
</template>

<script>
import previewTable from '@/components/previewTable';
import tableDrawer from '@/components/tableDrawer';
export default {
  components:{
        previewTable,
        tableDrawer
    },
    computed:{
      disableCoinSelect(){
        if(this.selectedCoin.length==5){
          return true
        }else{
        return false
         }
      }
       
    },
  data () {
    return {
      drawer:false,
      exten:false,
      betLimit:'10-1000',
      changenumbers: {
      '10-1000':{bet_limit:'1,000', banker:'1,000', player:'1,000', tie:'125', pair:'90'},
      '50-5000':{bet_limit:'5000', banker:'5,000', player:'5,000', tie:'625', pair:'454'},
      '100-5000':{bet_limit:'600', banker:'5,000', player:'5,000', tie:'625', pair:'454'},
      '100-10k':{bet_limit:'100', banker:'10,000', player:'10,000', tie:'1250', pair:'909'},
      '200-20k':{bet_limit:'200', banker:'20,000', player:'20,000', tie:'2500', pair:'1818'},
    },
      progress:50,
      window:1,
      coinMenu:false,
      selectedCoin:[],
      showingCoin:['5籌碼.png','10K籌碼.png','10籌碼.png','20K籌碼.png','50籌碼.png'],
      coinList:['5籌碼.png','10K籌碼.png','10籌碼.png','20K籌碼.png','20籌碼.png','50籌碼.png','100籌碼.png',
                '200籌碼.png','500籌碼.png','1000籌碼.png','2000籌碼.png','5000籌碼.png'],
      betCoin:'5籌碼.png',
      items: [
          { title: 'Dashboard', icon: 'dashboard' },
          { title: 'Account', icon: 'account_box' },
          { title: 'Admin', icon: 'gavel' },
        ],
            }
            },
  methods:{
      changeShowing(){
          this.showingCoin=[...this.selectedCoin]
          this.coinMenu=false
        },
      openCoinSelect(){
        this.selectedCoin=[...this.showingCoin]
      },
      cancelCoinSelect(){
        this.selectedCoin=[]
        this.coinMenu=false
      }
  }
}
</script>
<style scoped>
 .scroll {
      overflow-y: auto;
    }
    .playTable{
        background-image: url("/icon/荷官暫代圖.png");
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
        height:100%;
        cursor: url('/21.png') 2 2,auto
    }
    .selectCoin{
        width: 100%;
        background-color:black
    }
    .table-info{
      font-size: 0.8vw;
    }
    .room-list{
        font-size: 0.8vw;
    }
    .room-title{
        width:20%;
        height:5vh;
        position:absolute; 
        top:0;
        left:0; 
        background-color:rgba(0,0,0,0.5);
        font-size: 1vw;
    }
    .gameCountDown{
        position:absolute; 
        top:10%;
        left:5%;
    }
    .result-cards{
        background-color:rgba(0, 0, 0,0.8);
         position: relative;;
        width:100%; 
        height:100%
    }
    .tabActive{
      background-image:
      linear-gradient(
          rgb(255, 255, 255) 63%, 
          #B98F38
        );
      
    }
    .cardGradient{
      background-image:
      linear-gradient(
          rgb(255, 255, 255) 23%, 
          #B98F38
        );
    }
    .windowActive{
      background-color:#AA8647 ;
      
    }
    .Custombutton {
      border: none;
      color: white;
      padding: 9px;
      text-align: center;
      text-decoration: none;
      display: inline-block;
      font-size: 0.8vw;
      margin: 0px 8.5px;
      cursor: pointer;
      background-image:url('/icon/選擇桌台ui_1.png');
      background-repeat: no-repeat;
      background-position: center;
      background-size: 100% 100%;
      letter-spacing:20px;
      
    }
    .Custombutton:focus {
    outline: 1px solid #F7D8A8;
    outline-offset: -4px;
}
  
</style>
