<template>
  <v-container  class="pa-0 ma-1" fluid>
    <v-row no-gutters>

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
              <v-tab style="color:#b5a182;border-right:3px solid black;">
                All Baccarat
              </v-tab>
              <v-tab style="color:#b5a182;border-right:3px solid black;">
                Special Baccarat
              </v-tab>
              <v-tab>
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
                   <div class="dashboard-card" flat v-for="project in projects" :key="project.name">
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


              <v-tab-item :value="'navtab-' + 2">
                <v-card
                   flat
                   tile

                 >
                 <v-row style="width:100%;" class="pa-0 scrollbar" no-gutters>

                     <multibetRoadMap v-for="project in projects" :key="project.name" :project="project">

                     </multibetRoadMap>

                 </v-row>
                </v-card>
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
import multibetRoadMap from '@/components/multibet/multibetRoadMap';
import multibetSlite from '@/components/multibet/multibet1';
export default {
  components:{
    multibetRoadMap,
    multibetSlite
  },
data() {
  return {
    betLimit:'10-1000',
    projects: [
      {seri:'C01',name:'SIKEN',user: '123300', bb: '123', pp: '2300',tt: '2020', status:'Dealing'},
      {seri:'C02',name:'HONGLONG',user: '5200', bb: '123', pp: '20',tt: '2020', status:'Waiting'},
      {seri:'C03',name:'KUNHEAR',user: '2200', bb: '123', pp: '2320',tt: '2020', status:'12'},
      {seri:'C04',name:'CHEA_C',user: '2200', bb: '2200', pp: '2300',tt: '2020', status:'Player Win'},
      {seri:'C05',name:'MAkara',user: '2200', bb: '200', pp: '2320',tt: '2020', status:'Shuffling'},
      {seri:'C06',name:'HEAT_S',user: '2200', bb: '200', pp: '200',tt: '2020', status:'Waiting'},
      {seri:'C07',name:'SVEYNAR',user: '2200', bb: '1232', pp: '23220',tt: '2020', status:'12'},
      {seri:'C08',name:'CHANDA',user: '2200', bb: '12300', pp: '23',tt: '2020', status:'Shuffling'},
      {seri:'C09',name:'YORNNEN',user: '2200', bb: '1200', pp: '23200',tt: '2020', status:'Dealing'},
      {seri:'C10',name:'PHALLA',user: '2200', bb: '1200', pp: '23200',tt: '2020', status:'Waiting'},

    ],
    changenumbers: {
      '10-1000':{bet_limit:'10 - 1,000', banker:'1,000', player:'1,000', tie:'125', pair:'90'},
      '50-5000':{bet_limit:'50 - 5,000', banker:'5,000', player:'5,000', tie:'625', pair:'454'},
      '100-5000':{bet_limit:'100 - 5,000', banker:'5,000', player:'5,000', tie:'625', pair:'454'},
      '100-10k':{bet_limit:'100 - 10K', banker:'10,000', player:'10,000', tie:'1250', pair:'909'},
      '200-20k':{bet_limit:'200 - 20K', banker:'20,000', player:'20,000', tie:'2500', pair:'1818'},
    },
    favoriteshow: false,
    doneresult:false,
    headers: [
        {
          text: 'Table',
          align: 'start',

        },
        { text: 'Bet Content', value: 'category' },
        { text: 'Bet Amount', value: 'bet_amount' },
        { text: 'Win/Lose', value: 'winlose' },
        { text: 'Remark', value: 'remark' },
      ],
      desserts: [
        {
          name: '',
          category: '',
          bet_amount:'',

        },
        {
          name: '',
          category: '',
        },
        {
          name: '',
          category: '',
        },
        {
          name: '',
          category: '',
        },
        {
          name: '',
          category: '',
        },
        {
          name: '',
          category: '',
        },
        {
          name: '',
          category: '',
        },

        {
          name: '',
          category: '',
        },
      ],

  }
}
}
</script>

<style scoped>
.dashboard-card {
    background-color:white;
    height: 44px;
    margin-top: 2px;
}

.playTable{
    background-image: url("/icon/荷官暫代圖.png");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 33vh;
    margin: 0;
    padding: 0;
}
.changepicture {
  background-color: #b9934e;
  height: 9vh;
  width: 100%;
  margin-top:0.1vh;
}

.tabform{
  height: 42px;
}

.scrollbar {
   height: 97vh;
  overflow-y: scroll;
}

</style>
