<template>
  <v-app id="app">
    <v-navigation-drawer
      fixed
      app
      dark
      permanent
      width="10vw"
      color="rgba(0, 0, 0, 0.8)"
    >
    <v-img :aspect-ratio="16/10" src="https://cdn.vuetifyjs.com/images/parallax/material.jpg">
        <v-row align="end" class="lightbox white--text pa-2 fill-height">
          <v-col>
            <div class="subheading">Logo</div>
            <div class="body-1">Logo</div>
          </v-col>
        </v-row>
      </v-img>
      <v-list
      >
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          class="red--text text-center"
        >
          <v-list-item-content style="padding:5px" >
          <v-btn block
          height="5vh"
          :to="item.to"
          class="text-size"
          >
          {{item.title}}
          </v-btn>
          </v-list-item-content>
          <!-- <v-btn block
          >{{item.title}}</v-btn> -->
        </v-list-item>
      </v-list>
      <template v-slot:append>
           <v-list>
        <!-- <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
          class="red--text text-center"
        >
          <v-list-item-content >
            <v-list-item-title ><v-icon>{{ item.icon }}</v-icon> {{item.title}}</v-list-item-title>
          </v-list-item-content>

        </v-list-item> -->
        <v-divider/>
        <v-list-item
          link
          class="red--text text-center ">
           <v-list-item-content >
            <v-list-item-title class="text-size"><v-icon>email</v-icon> blah blah</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider/>
        <v-list-item
        class="red--text text-center"
        link >
           <v-list-item-content >
            <v-list-item-title class="text-size" ><v-icon>people</v-icon> blah blah</v-list-item-title>
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
    <v-content>

        <nuxt />

    </v-content>
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
    color="rgba(0, 0, 0, 0.8)"
    padless
    height="40px"
    inset
    app
    dark
    >
    <v-row  class="d-flex flex-row justify-end">
       <v-divider vertical/>
      <div class="d-flex justify-center">
        <v-btn icon class="pa-2 ma-1">
          <v-icon class="pa-2" v-show="soundOn">audiotrack</v-icon>
          <v-icon class="pa-2" v-show="!soundOn">music_off</v-icon>
        </v-btn>
      </div>

      <v-divider vertical/>
      <div class="d-flex" style="width:175px">
        <v-btn icon class="pa-2 ma-1">
        <v-icon class="pa-2 ">volume_up</v-icon>
        </v-btn>
         <v-btn icon class="pa-2 ma-1">
        <v-icon class="pa-2 ">view_list</v-icon>
        </v-btn>
         <v-btn icon class="pa-2 ma-1">
        <v-icon class="pa-2 ">view_module</v-icon>
        </v-btn>
         <v-btn icon class="pa-2 ma-1">
        <v-icon class="pa-2 ">view_column</v-icon>
        </v-btn>
      </div>
      <v-divider vertical/>
      <div class="d-flex" style="width:165px">
        <div style="width:40px" class="pa-2">

           <v-icon>attach_money</v-icon>

        </div>

        <div  class="pa-2" style="width:75px">
          5,00000
        </div>

        <div class=" pa-2" >
            <v-icon small>autorenew</v-icon>
        </div>


      </div>
      <v-divider vertical/>
       <div class="d-flex" style="width:180px">
          <div style="width:40px" class="pa-2">
           <v-icon>account_circle</v-icon>
           </div>
        <div class="pa-2" style="width:75px">
            PLAYER_NAME
        </div>
       </div>
        <v-divider vertical/>
        <div class="d-flex" style="width:250px">
          <div class="pa-2">
          2020-07-14 10:46:34 (UTC+6.5)
          </div>
        </div>
         <v-divider vertical/>
          <div class="d-flex justify-center">
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
              <v-icon class="pa-2">menu</v-icon>
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
          <div class="d-flex" style="width:100px">
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
  data () {
    return {
      fixed: false,
      soundOn:true,
      betlogDialog:false,
      memberReportDialog:false,
      gameAgreementDialog:false,
      settingDialog:false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/Dashboard/dashboard'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'blabhlbabh',
          to: '/inspire'
        },
         {
          icon: 'mdi-chart-bubble',
          title: 'MULTI-BET',
          to: '/Dashboard/complete_view'
        },
         {
          icon: 'mdi-chart-bubble',
          title: 'blabhlbabh',
          to: '/inspire'
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
#app {
    background-color: var(--v-background-base);
}
</style>
