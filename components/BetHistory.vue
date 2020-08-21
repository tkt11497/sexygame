<template>
<span>
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
              <div class="text-center" style="height:45vh; width:100%;background-color:black">
                <div style="width:100%; height:30%">
                <PreviewTable :row="6" :column="36"/>
                </div>
                <v-divider/>
                <div style="width:100%; height:10%">
                  <PreviewTable :row="3" :column="36"/>
                </div>
                <v-divider/>
                <v-row style="width:100%; height:10%" no-gutters>
                  <div style="width:49.7%; height:100%; ">
                  <PreviewTable :row="3" :column="16"/>
                  </div>
                  <v-divider vertical/>
                  <div style="width:50%; height:100%">
                    <PreviewTable :row="3" :column="16"/>
                  </div>
                </v-row>
                <v-divider/>
                <div style="width:100%; height:40%">
                  <PreviewTable :row="6" :column="18"/>
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
</span>
</template>
<script>
export default {
    data(){
      return{
        window:1,
      }
    }
}
</script>
<style scoped>
 .windowActive{
      background-color:#AA8647 ;
      
    }
      .room-list{
        font-size: 0.8vw;
    }
</style>