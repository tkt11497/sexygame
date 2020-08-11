<template>
  <v-container class="ma-0 ml-1" fluid>
    <v-row >
      <!-- Main First Col -->
      <v-col cols="8" style="padding:0;" >

            <v-tabs
              fixed-tabs
              background-color=#404040
              dark
              active-class="white black--text"
            >
              <v-tab href="#navtab-1" style="color:#b5a182;border-right:3px solid black;" v-if="favoriteshow">
                My favorite
              </v-tab>

              <v-tab href="#navtab-2" style="color:#b5a182;border-right:3px solid black;">
                All Games
              </v-tab>

              <v-tab style="color:#b5a182; border-right:3px solid black;">
                All Baccarat
              </v-tab>

              <v-tab style="color:#b5a182; border-right:3px solid black;">
                Special Baccarat
              </v-tab>

              <v-tab style="color:#b5a182;">
                Other Games
              </v-tab>


            <!-- Start favorite  -->
            <v-tab-item :value="'navtab-' + 1">
              <v-card
                 flat
                 tile

               >
               <div>
                   <v-col tile cols="12">
                     <v-card v-if="favoriteshow" @click="favoriteshow=false">
                     <div class="dashboard-card" v-if="project.name === 'SIKEN'" flat v-for="project in projects" :key="project.name">
                         <v-layout>
                           <v-flex mt-3 mb-2 ml-5>
                             <span class="black--text">Seri {{ project.seri}}</span>
                           </v-flex>
                                 <v-flex mt-3 mb-2>
                                     <span class="red--text">庄</span>
                                     <span class="black--text">{{project.bb}}</span>
                                 </v-flex>
                                   <v-flex mt-3 mb-2>
                                     <span class="blue--text " >圓</span>
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

                                         <v-flex mt-2 mb-1>
                                           <v-icon medium color="#c3a475">switch_video</v-icon>
                                         </v-flex>

                                         <v-flex>
                                               <div class="white--text" style="background:#c6c6c9; height:44px;">
                                                 <div> {{project.status}} </div>
                                               </div>
                                         </v-flex>
                               </v-layout>
                       </div>

                       <v-img

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
                 </v-col>
               </div>
              </v-card>
            </v-tab-item>
  <!-- End Favorite -->


    <!-- card panel -->
    <v-tab-item :value="'navtab-' + 2">
              <v-card>
                <div class="dashboard-card" v-if="project.name === 'SIKEN'" flat v-for="project in projects" :key="project.name">
                    <v-layout>
                      <v-flex mt-3 mb-2 ml-5>
                        <span class="black--text">Seri {{ project.seri}}</span>
                      </v-flex>

                                <div class="mt-3 mb-2 mr-1">
                                  <span class="red--text">庄</span>
                                  <span class="black--text mr-3">{{project.bb}}</span>
                                </div>


                                <div class="mt-3 mb-2 mr-1">
                                  <span class="blue--text">圓</span>
                                  <span class="black--text mr-3">{{project.pp}}</span>
                                </div>

                                <div class="mt-3 mb-2 mr-1">
                                  <span class="green--text">和</span>
                                  <span class="black--text mr-3">{{project.tt}}</span>
                                </div>


                                <div class="black--text mt-3 mb-2 mr-1">
                                  <span class="red--text mt-3 mb-2 mr-1">庄庄</span>
                                  {{project.tt}}
                                </div>


                                <div class="black--text mt-3 mb-2 ml-2">
                                  <span class="blue--text">和和</span>
                                  {{project.tt}}
                                </div>

                                    <div class="mt-2 mb-2 ml-2" >
                                      <v-btn class="white--text" small  color="#c70000">庄問路</v-btn>
                                    </div>
                                    <div class="ma-2 mt-3">
                                      <v-img
                                          max-width="1vw"
                                          max-height="1vw"
                                          src="/icon/大紅圈.png"
                                        />
                                    </div>

                                    <div>
                                      <v-avatar color="#c70000" class="mt-3 mr-2" size="15">
                                      </v-avatar>
                                    </div>

                                    <div class="ma-2 mt-2">
                                      <span class="font-weight-bold red--text ">/</span>
                                    </div>

                                    <div class="mt-2 mb-2 ml-2" >
                                      <v-btn class="white--text" small color="#2d30b1">
                                          閒問路
                                      </v-btn>
                                    </div>

                                    <div class="ma-2 mt-3">
                                      <v-img
                                          max-width="1vw"
                                          max-height="1vw"
                                          src="/icon/大藍圈.png"
                                        />
                                    </div>

                                    <div>
                                      <v-avatar color="#2d30b1" class="mt-3 mr-2" size="15">
                                      </v-avatar>
                                    </div>

                                    <div class="ma-2 mt-2">
                                      <span class="font-weight-bold" style="color:#2d30b1">/</span>
                                    </div>

                                    <v-spacer></v-spacer><v-spacer></v-spacer>

                                    <v-flex mt-1 mb-1>
                                      <v-btn icon medium color="#787878">
                                          <v-icon>favorite</v-icon>
                                      </v-btn>
                                    </v-flex>

                                    <v-flex mt-1 mb-1>
                                      <v-btn icon medium color="#c3a475">
                                          <v-icon>switch_video</v-icon>
                                      </v-btn>
                                    </v-flex>

                                    <v-flex mb-4>
                                          <div class=" d-flex justify-center align-center black--text" style="background:#c6c6c9; height:50px;">
                                            <div> {{project.status}} </div>
                                          </div>
                                    </v-flex>
                          </v-layout>
                  </div>



              <v-row no-gutters>
              <v-col  cols="8">
                <v-card class="result-cards"
                  height="100%"
                >
                    <img
                    src="/card/黑桃J.png"
                     style="width:3.7vw; height:11.3vh; position:absolute;left:4%;bottom:25%"/>

                    <img
                    src="/card/黑桃K.png"
                     style="width:3.7vw; height:11.3vh; position:absolute;left:14%;bottom:25%"/>
                    <img
                    src="/card/紅心J.png"
                     style="width:3.7vw; height:11.3vh; position:absolute;left:24%;bottom:25%"/>
                    <div
                    class=" d-flex justify-center align-center"
                    style="width:13%; height:17%; position:absolute; top:79%; left:11%; background-color:blue">
                        <span>P 01</span>
                    </div>
                    <div
                    class=" d-flex justify-center align-center"
                    style="width:28%; height:55%; position:absolute; top:17%; left:36%; background-color:red; font-size:1.8vw">
                        <span>Banker Win</span>
                    </div>
                    <img
                    src="/card/梅花J.png"
                     style="width:3.7vw; height:11.3vh; position:absolute;right:3.5%;bottom:26%"/>

                    <img
                    src="/card/梅花K.png"
                     style="width:3.7vw; height:11.3vh; position:absolute;right:13.8%;bottom:26%"/>
                    <img
                    src="/card/梅花Q.png"
                     style="width:3.7vw; height:11.3vh; position:absolute;right:24%;bottom:26%"/>
                   <div
                   class=" d-flex justify-center align-center"
                   style="width:13%; height:17%; position:absolute; right:10%; background-color:red; bottom:5%">
                       <span>B 8</span>
                   </div>

                </v-card>
              </v-col>
              <v-col cols="4">
                <v-tabs class="tabform"
                v-model="tab"
                background-color="#404040 accent-4;"
                centered
                dark
                icons-and-text
                active-class="orange lighten-4 black--text"
                fixed-tabs
                height="39"
                >


                <v-tab href="#tab-1" >
                Baccarat
                </v-tab>

                <v-tab href="#tab-2">
                Commission
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
                        <v-col tile cols="4" class="playArea-tile" align="center">
                          <h3>Player</h3>
                        </v-col>
                        <v-col tile cols="4" class="playArea-tile tile" align="center">
                          <h3> Tie</h3>
                        </v-col>
                        <v-col tile cols="4" class="playArea-tile banker" align="center">
                          <h3> Banker</h3>
                        </v-col>
                      </v-row>
                      <v-row style="margin:0;">
                        <v-col tile cols="4" class="playArea-tile" align="center">
                           <h3>P.Pair</h3>
                        </v-col>
                        <v-col tile cols="4" class="playArea-tile tile" align="center">
                           <h3>Lucky Six</h3>
                        </v-col>
                        <v-col tile cols="4" class="playArea-tile banker" align="center">
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
                        <v-col tile cols="4" class="playArea-tile" align="center">
                          <h3>Player</h3>
                        </v-col>
                        <v-col tile cols="4" class="playArea-tile tile" align="center">
                          <h3> Tie</h3>
                        </v-col>
                        <v-col tile cols="4" class="playArea-tile banker" align="center">
                          <h3> Banker</h3>
                        </v-col>
                      </v-row>
                      <v-row style="margin:0;">
                        <v-col tile cols="4" class="playArea-tile" align="center">
                           <h3>P.Pair</h3>
                        </v-col>
                        <v-col tile cols="4" class="playArea-tile tile" align="center">
                           <h3>Lucky Six</h3>
                        </v-col>
                        <v-col tile cols="4" class="playArea-tile banker" align="center">
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
              </v-col>

              </v-row>

            </v-card>

            <!-- end card panel -->


                <multibetindex v-for="project in projects" :key="project.name" :project="project">

                </multibetindex>
            </v-tab-item>
          </v-tabs>
      </v-col>
<!-- End Main First Col -->


        <!-- Main Second Col -->
            <v-col  cols="4" style="padding:0;">

              <multibetSlite></multibetSlite>

            </v-col>
        <!-- End Main Second Col -->


  </v-row>
  </v-container>
</template>

<script>
import multibetindex from '@/components/multibet/multibetindex';
import multibetSlite from '@/components/multibet/multibet1';
export default {
  components:{
    multibetindex,
    multibetSlite
  },
data() {
  return {
    projects: [
      {seri:'C01',name:'SIKEN',user: '123300', bb: '123', pp: '2322200',tt: '2020', status:'Dealing'},
      {seri:'C02',name:'HONGLONG',user: '5200', bb: '123', pp: '2322200',tt: '2020', status:'Waiting'},
      {seri:'C03',name:'KUNHEAR',user: '2200', bb: '123', pp: '2322200',tt: '2020', status:'12'},
      {seri:'C04',name:'CHEA_C',user: '2200', bb: '123', pp: '2322200',tt: '2020', status:'Player Win'},
      {seri:'C05',name:'MAkara',user: '2200', bb: '123', pp: '2322200',tt: '2020', status:'Shuffling'},
      {seri:'C06',name:'HEAT_S',user: '2200', bb: '1232', pp: '2322200',tt: '2020', status:'Waiting'},
      {seri:'C07',name:'SVEYNAR',user: '2200', bb: '322', pp: '2322200',tt: '2020', status:'12'},
      {seri:'C08',name:'CHANDA',user: '2200', bb: '1232', pp: '2322200',tt: '2020', status:'Shuffling'},
      {seri:'C09',name:'YORNNEN',user: '2200', bb: '123', pp: '2322200',tt: '2020', status:'Dealing'},
      {seri:'C10',name:'PHALLA',user: '2200', bb: '1232', pp: '2322200',tt: '2020', status:'Waiting'},

    ],
     favoriteshow: false,
  }
},
    // methods:{
    //   favoritecatch() {
    //     this.$emit('favoriteshow')
    //   }
    // }
}
</script>

<style scoped>

.changenumber {
  background-color: #b9934e;
  height: 9vh;
  width: 100%;
  margin-top:0.1vh;
}

.result-cards {
  background-color: gray;
  position: relative;
}


</style>
