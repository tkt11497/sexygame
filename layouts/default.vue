<template>
  <v-app id="app">
    <v-navigation-drawer
      fixed
      app
      permanent
      width="9vw"
      style="box-sizing: border-box;border-right: 0.5vw solid #A56F19;"
    >
    <div style="height:30%;width:100% ;position:relative">
      <h1   style="position:absolute; 
            bottom:15%; left: 50%;
            transform: translate(-50%, -50%);
            font-size:1vw;
            font-weight:bold"> 
            L O G O
       </h1> 
      <p style="position:absolute; bottom:1%;font-size:0.8vw;left: 50%;
            transform: translate(-50%, -50%);
            font-weight:bold"> 
            <pre>Company Name</pre>
      </p>
    </div>
         
         <router-link
          v-for="(item, i) in items"
          :key="i"
          :to="item.to" 
          v-slot="{ navigate, isActive }" 
          
        >
        
            <v-btn 
                  block
                  height="6vh"
                  class="text-size mt-2" 
                  dark 
                  elevation="18"   
                  :class="[isActive && 'activeLink']"
                  @click="navigate"
                  
                  >
              {{item.title}} 
              
            </v-btn>
        </router-link>
        
      <template v-slot:append>
           <v-list>
        <v-divider/>
        <v-list-item
          link
          class="red--text text-center ">
           <v-list-item-content >
            <v-list-item-title class="text-size"><v-icon>email</v-icon> Feedback</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider/>
        <v-list-item
        class="red--text text-center"
        link >
           <v-list-item-content >
            <v-list-item-title class="text-size" ><v-icon>people</v-icon> 12,213</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider/>
        <v-list-item class="red--text text-center" link>
           <v-list-item-content >
            <v-list-item-title class="text-size" >app-123beta</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

      </v-list>
        </template>
    </v-navigation-drawer>
    <!-- <v-app-bar
      flat
      fixed
      app
      height="20px"
    >

      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar> -->
    <v-main >

        <nuxt  />

    </v-main>
    <v-dialog
      v-model="betlogDialog"
      max-width="1200" 
      min-width="290"
    >
      <betLog @close="betlogDialog=false"/>
    </v-dialog>
    <v-dialog
      v-model="memberReportDialog"
      max-width="800" 
      min-width="290"
    >
      <memberReport @close="memberReportDialog=false"/>
    </v-dialog>
    <v-dialog
      v-model="gameAgreementDialog"
      max-width="800" 
      min-width="290"
    >
      <gameAgreement @close="gameAgreementDialog=false"/>
    </v-dialog>
     <v-dialog
      v-model="settingDialog"
      max-width="800" 
      min-width="290"
    >
      <setting @close="settingDialog=false"/>
    </v-dialog>
    <v-footer
        color="#FFFFFF"
        padless
        height="40px"
        inset
        fixed 
         
        elevation="20" 
    >
          <v-row  class="d-flex flex-row justify-end">
            
             <div class="d-flex justify-center">
                <v-btn icon class="pa-2 ma-1" link exact v-if="showViewList">
               <v-img src="/icon/wifi按鈕_4.png"></v-img>
              </v-btn>
             </div>
             <v-divider vertical/>
            <div class="d-flex justify-center">
                <v-menu
                  offset-y
                  top 
                  :close-on-content-click="false"
                  :nudge-width="350"
                  :max-width="350"
                  >
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn icon class="pa-2 ma-1"  
                    v-bind="attrs"
                    v-on="on">
                      <v-icon class="pa-2" v-show="music!=0" color="#B98F38">audiotrack</v-icon>
                      <v-icon class="pa-2" v-show="music==0" color="#B98F38">music_off</v-icon>
                    </v-btn>
                  </template>
                      <v-card color="rgba(34, 34, 34,0.9)">
                        <v-row no-gutters>
                            <v-col cols="3" class="text-center">
                              <p style="color:#C4A76E" class="mt-4">Music</p>
                            </v-col>
                    
                            <v-col cols="9" class="text-center">
                            <v-row no-gutters dense >
                                <v-btn icon color="#C4A76E" class="mt-2" @click="music==0?music=50:music=0">
                                <v-icon v-show="music!=0">volume_up</v-icon>
                                <v-icon v-show="music==0">volume_off</v-icon>
                                </v-btn>
                                <v-slider
                                    v-model="music" 
                                    class="mt-3" 
                                    color="#196260"
                                ></v-slider>
                            </v-row>
                        </v-col>
                        </v-row>
                      </v-card>
                  
                </v-menu>
            </div>

            <v-divider vertical/>
            <div class="d-flex justify-center align-center" style="width:10vw">
              <v-menu
                  offset-y
                  top 
                  :close-on-content-click="false"
                  :nudge-width="350"
                  :max-width="350"
                  >
                  <template v-slot:activator="{ on, attrs }">
                      <v-btn icon 
                      v-bind="attrs"
                        v-on="on">
                      <v-icon class="pa-2 " color="#B98F38">volume_up</v-icon>
                      </v-btn>
                  </template>
                  <v-card color="rgba(34, 34, 34,0.9)">
                        <v-row no-gutters>
                            <v-col cols="4" class="text-center">
                              <p style="color:#C4A76E" class="mt-4">Studio Sound</p>
                            </v-col>
                    
                            <v-col cols="8" class="text-center">
                            <v-row no-gutters dense >
                                <v-btn icon color="#C4A76E" class="mt-2" @click="studioSound==0?studioSound=50:studioSound=0">
                                <v-icon v-show="studioSound!=0">volume_up</v-icon>
                                <v-icon v-show="studioSound==0">volume_off</v-icon>
                                </v-btn>
                                <v-slider
                                    v-model="studioSound" 
                                    class="mt-3" 
                                    color="#196260"
                                ></v-slider>
                            </v-row>
                        </v-col>
                        </v-row>
                        <v-row no-gutters>
                            <v-col cols="4" class="text-center">
                                  <p style="color:#C4A76E" class="mt-4">Game Volume</p>
                            </v-col>
                    
                            <v-col cols="8" class="text-center">
                                <v-row no-gutters dense >
                                    <v-btn icon color="#C4A76E" class="mt-2" @click="gameVolume==0?gameVolume=50:gameVolume=0">
                                    <v-icon v-show="gameVolume!=0">volume_up</v-icon>
                                    <v-icon v-show="gameVolume==0">volume_off</v-icon>
                                    </v-btn>
                                    <v-slider
                                        v-model="gameVolume" 
                                        class="mt-3" 
                                        color="#196260" 
                                    ></v-slider>
                                </v-row>
                            </v-col>
                        </v-row>
                      </v-card>
              </v-menu>
              <v-btn icon  link :to="toRouteName+'/default'" exact v-if="!showViewList">
              <v-icon class="pa-2 " color="#B98F38">view_list</v-icon>
              </v-btn>
              <v-btn icon  link :to="toRouteName+'/road_map_view'" exact v-if="!showViewList">
              <v-icon class="pa-2 " color="#B98F38">view_module</v-icon>
              </v-btn>
              <v-btn icon  link :to="toRouteName+'/big_road_view'" exact v-if="!showViewList">
              <v-icon class="pa-2 " color="#B98F38">view_column</v-icon>
              </v-btn>


              <v-btn icon class="pa-2 ma-1" link  exact v-if="showViewList">
              <v-img src="/icon/高清按鈕.png"></v-img>
              </v-btn>
              <v-btn icon class="pa-2 ma-1" link exact v-if="showViewList">
              <v-icon class="pa-2 " color="#B98F38">videocam</v-icon>
              </v-btn>
              <v-btn icon class="pa-2 ma-1" link exact v-if="showViewList&&false">
              <v-icon class="pa-2 " color="#B98F38">videocam_off</v-icon>
              </v-btn>
               <v-btn icon class="pa-2 ma-1" link exact v-if="showViewList">
               <v-img src="/icon/重新載入視訊按鈕.png"></v-img>
              </v-btn>
            </div>
            <v-divider vertical/>
            <div class="d-flex justify-center align-center footer-size" style="width:8vw">
              

                <v-icon color="#B98F38" class="mr-2">attach_money</v-icon>

             
                5,00000
            
                  <v-icon small color="#B98F38" class="ml-2">autorenew</v-icon>
             


            </div>
            <v-divider vertical/>
            <div class="d-flex justify-center align-center footer-size" style="width:10vw">
                
                <v-icon class="mr-1" color="#B98F38">account_circle</v-icon>
               
             
                  PLAYER_NAME
             
            </div>
              <v-divider vertical/>
              <div class="d-flex justify-center align-center footer-size" style="width:14vw">
                
                2020-07-14 10:46:34 (UTC+6.5)
              
              </div>
              <v-divider vertical/>
                <div class="d-flex justify-center align-center">
                  <v-menu
                  offset-y
                  top
                  close-on-content-click
                  :nudge-width="100"
                  left
                  :max-width="250"
                  >
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                icon
                class="pa-2 ma-1"
                v-bind="attrs"
                  v-on="on"
                >
                    <v-icon class="pa-2" color="#B98F38">menu</v-icon>
                  </v-btn>
              </template>


              <v-card>
                    <v-list
                    dark
                    color="rgba(12, 10, 6, 0.8)">
                      <v-subheader>
                        <v-icon>account_circle</v-icon>PLAYER_NAME
                      </v-subheader>
                  <v-list-item link @click="betlogDialog=true">
                    <v-list-item-icon>
                      <v-icon >history</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>Bet Log  </v-list-item-content>
                  </v-list-item>

                  <v-list-item link @click="memberReportDialog=true">
                    <v-list-item-icon>
                      <v-icon >text_snippet</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>Member Report</v-list-item-content>
                  </v-list-item>
                  <v-list-item link @click="settingDialog=true">
                    <v-list-item-icon>
                      <v-icon >settings</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>Settings</v-list-item-content>
                  </v-list-item>
                  <v-list-item link @click="gameAgreementDialog=true">
                    <v-list-item-icon>
                      <v-icon >info</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>Game Agreement</v-list-item-content>
                  </v-list-item>
                  <v-list-item>
                  <v-list-item-action-text>
                    v0.123
                  </v-list-item-action-text>
                  </v-list-item>

                </v-list>
              </v-card>
            </v-menu>
                </div>
              <v-divider vertical/>
                <div class="d-flex" style="width:8vw">
                </div>





          </v-row>
    </v-footer>
  </v-app>
</template>

<script>
import betLog from '@/components/bet_log';
import memberReport from '@/components/member_report';
import gameAgreement from '@/components/gameAgreement';
import setting from '@/components/setting';
export default {
   components:{
        betLog,
        memberReport,
        gameAgreement,
        setting
    },
    computed: {
   
    toRouteName() {
        let routeArr=  this.$route.name.split('-')
        if(routeArr.includes("multibet")){
          return '/multibet'
        }else{
        return '/roomlist';
        }
    },
    showViewList(){
        let routeArr= this.$route.name.split('-')
        console.log(routeArr)
        if(routeArr.includes("betRoom")){
          return true
        }else{
        return false;
        }
    }
  },
  data () {
    return {
      studioSound:50,
      gameVolume:60,
      music:30,
      fixed: false,
      soundOn:true,
      betlogDialog:false,
      memberReportDialog:false,
      gameAgreementDialog:false,
      settingDialog:false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'BACCARAT',
          to: '/roomlist/default'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Other Games',
          to: '/inspire'
        },
         {
          icon: 'mdi-chart-bubble',
          title: 'MULTI-BET',
          to: '/multibet/default'
        },
         {
          icon: 'mdi-chart-bubble',
          title: 'Mobile',
          to: '#'
        }

      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
<style scoped>
.text-size{
  font-size: 1.6vh;
}
.footer-size{
  font-size: 0.8vw;
}
#app {
    background-color: var(--v-background-base);
}
.activeLink{
  background-image:
  linear-gradient(
      rgb(255, 255, 255) 63%, 
      #B98F38
    );
  color:black
}
</style>
