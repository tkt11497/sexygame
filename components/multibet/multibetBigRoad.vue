<template>
  <v-flex md3>
    <!-- Start card -->
      <v-card class="ml-1 mt-1 mr-1" >
          <div>
              <v-row no-gutters>
                <v-col>

                    <v-flex row pa-0 ma-0 style="background:#665b4b">
                      <span class="ml-1 mt-1">Seri {{ project.seri}}</span>
                    <v-spacer></v-spacer><v-spacer></v-spacer><v-spacer></v-spacer><v-spacer></v-spacer><v-spacer></v-spacer><v-spacer></v-spacer><v-spacer></v-spacer><v-spacer></v-spacer><v-spacer></v-spacer><v-spacer></v-spacer><v-spacer></v-spacer>

                      <v-btn @click="favoriteshow=true" text icon medium color="#787878"><v-icon>favorite</v-icon></v-btn>
                    </v-flex>

                  <v-row style="height:30px;">
                    <v-flex mt-1 mb-2 pl-3>
                        <span class="red--text">庄</span>

                      <span>{{project.bb}}</span>
                    </v-flex>
                      <v-flex mt-1 mb-2 mr-2>
                        <span class="blue--text">圓</span>
                          <span>{{project.pp}}</span>
                      </v-flex>
                            <v-flex mt-1 mb-2 mr-2>
                              <div>
                                <span class="green--text">和</span>
                                {{project.tt}}
                              </div>
                            </v-flex>
                            <v-flex mb-1  mr-2>
                              <v-icon medium color="#c3a475">switch_video</v-icon>
                            </v-flex>
                            <v-flex mb-1 >
                                  <div class="d-flex justify-center align-center white--text mr-3" style="background:#c6c6c9; height:30px;">
                                     {{project.status}}
                                  </div>
                            </v-flex>

                  </v-row>

                  <v-flex row pa-0 ma-0>

                    <v-img
                    height="100%"

                        src="/icon/珠盤路單(小).png"
                    >

                  </v-img>

                  </v-flex>

                  <v-flex row pa-0 ma-0>
                    <v-tabs class="tabform"
                    fixed-tabs
                    v-model="tab"
                    background-color="#404040 accent-4"
                    centered
                    height="35"
                    active-class="orange lighten-4 black--text"
                    dark
                    icons-and-text
                    >
                    <v-tabs-slider></v-tabs-slider>

                    <v-tab href="#tab-1">
                    Bacc
                    </v-tab>

                    <v-tab href="#tab-2">
                     Commis
                    </v-tab>

                    <v-tab href="#tab-3">
                    Cow ?
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
                            <v-col tile cols="4" class="playArea-tile-last" style="color:#3470A9;" align="center">
                              <h3>Player</h3>
                            </v-col>
                            <v-col tile cols="4" class="playArea-tile-last tile" align="center">
                              <h3> Tie</h3>
                            </v-col>
                            <v-col tile cols="4" class="playArea-tile-last banker" align="center">
                              <h3> Banker</h3>
                            </v-col>
                          </v-row>
                        </div>
                      </v-card>
                    </v-tab-item>
                 </v-tabs>
               </v-flex>
                </v-col>

              </v-row>
            </div>
        </v-card>
    <!-- End card -->
  </v-flex>
</template>

<script>
  export default {
    props: ['project']
  }
</script>

<style scoped>
.playArea-tile{
    border:1px solid rgba(255,255,255, 0.3);
    color:#3470A9;
    height: 64px;

}
.playArea-tile-last{
  border:1px solid rgba(255,255,255, 0.3);
  color:#3470A9;
  height: 127px;
}


.banker{
  color:red
}

.tie{
  color:#0C930A;
}

.tile{
  color:green;

}

.playArea{
    background-color:rgb(3, 62, 29);
    height:128px;
}
</style>
