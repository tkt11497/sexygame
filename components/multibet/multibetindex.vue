<template>

  <!-- card panel -->
    <v-card class="mt-3">
      <div class="dashboard-card" >
          <v-layout>
            <v-flex mt-3 mb-2 ml-5>
              <span class="black--text">Seri {{ project.seri}}</span>
            </v-flex>

                      <div class="mt-3 mb-2 mr-1">
                        <span class="red--text">庄</span>
                        <span class="black--text mr-3">{{project.bb}}</span>
                      </div>


                      <div class="mt-3 mb-2 mr-1">
                        <span class="blue--text">和</span>
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
                            <v-btn @favoritecatch="favoriteshow=true" icon medium color="#787878">
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
      <v-img
      height="100%"

          src="/icon/珠盤路單(大).png"
      >

    </v-img>
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


</template>

<script>
  export default {
    props: ['project'],
    // favoriteshow: false,
    methods: {
      favoritecatch() {
        this.$emit('favoriteshow')
      }
    }
  }
</script>

<style scoped>
.dashboard-card {
    background-color:white;
    height: 49px;
    margin-top: 5px;
    /* border: 5px solid #e5e8e7; */

}
.playArea{
    background-color:rgb(3, 62, 29);
    height:128px;
}

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
  color:green
}


</style>
