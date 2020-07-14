<template>
  <v-app>
    <v-navigation-drawer
      
      fixed
      app
      dark
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
          height="50px"
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
          class="red--text text-center">
           <v-list-item-content >
            <v-list-item-title ><v-icon>email</v-icon> blah blah</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider/>
        <v-list-item 
        class="red--text text-center"
        link >
           <v-list-item-content >
            <v-list-item-title ><v-icon>people</v-icon> blah blah</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider/>
        <v-list-item class="red--text text-center" link>
           <v-list-item-content >
            <v-list-item-title >app-123beta</v-list-item-title>
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
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
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
            <v-btn icon class="pa-2 ma-1">
              <v-icon class="pa-2">menu</v-icon>
            </v-btn>
          </div>
         <v-divider vertical/>
          <div class="d-flex" style="width:100px">
          </div>
        <v-divider vertical/>


      
      
    </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      fixed: false,
      soundOn:true,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'blabhlbabh',
          to: '/inspire'
        },
         {
          icon: 'mdi-chart-bubble',
          title: 'blabhlbabh',
          to: '/inspire'
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
