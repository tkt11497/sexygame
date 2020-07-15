<template>
  <v-container class="pa-1 ma-0">
    <v-row>
      <v-col cols="8">
          <v-tabs
            fixed-tabs
            background-color=#1c170e
            dark
            active-class="brown darken-4 text--accent-4"
          >
            <v-tab>
              All Games
            </v-tab>
            <v-tab>
              All Baccarat
            </v-tab>
            <v-tab>
              Special Baccarat
            </v-tab>
            <v-tab>
              Other Games
            </v-tab>
          </v-tabs>


            <div  v-if="project.name === 'SIKEN'" flat v-for="project in projects" :key="project.name">
              <div class="dashboard-card">
                <v-layout>
                  <v-flex mt-3 mb-2>
                    <span class="white--text">Seri {{ project.seri}}</span>
                  </v-flex>
                        <v-flex mt-3 mb-2>
                            <span class="red--text">B</span>

                          <span class="white--text">{{project.bb}}</span>
                        </v-flex>
                          <v-flex mt-3 mb-2>
                            <span class="blue--text " >P</span>
                              <span class="white--text">{{project.pp}}</span>
                          </v-flex>
                                <v-flex mt-3 mb-2>
                                  <div class="white--text">
                                    <span class="green--text">T</span>
                                    {{project.tt}}
                                  </div>
                                </v-flex>
                                <v-flex mt-3 mb-2>
                                  <div class="white--text">
                                    <span class="red--text">BP</span>
                                    {{project.tt}}
                                  </div>
                                </v-flex>
                                <v-flex mt-3 mb-2>
                                  <div class="white--text">
                                    <span class="blue--text">PP</span>
                                    {{project.tt}}
                                  </div>
                                </v-flex>
                                <v-flex mt-2 mb-1  >
                                  <v-btn class="white--text" small  color="#c70000">Ask B.</v-btn>
                                </v-flex>
                                <v-flex mt-2 mb-1 >
                                  <v-btn class="white--text" small color="#2d30b1">
                                      Ask P.
                                  </v-btn>
                                </v-flex><v-spacer></v-spacer><v-spacer></v-spacer>
                                <v-flex mt-2 mb-1>
                                  <v-icon medium color="#787878">favorite</v-icon>
                                </v-flex>
                                <v-flex mt-2 mb-1>
                                  <v-icon medium color="#c3a475">switch_video</v-icon>
                                </v-flex>

                                <v-flex>
                                      <div class="white--text" style="background:#196260; height:50px;">
                                        <div> {{project.status}} </div>
                                      </div>
                                </v-flex>
                      </v-layout>
              </div>
          </div>


          <v-row>
            <div style="background:gray; margin-left:12px;">
              <v-column>
                <v-img
                  height="200"
                  width="693"
                ></v-img>
              </v-column>
            </div>

            <div>
              <v-column>

                      <v-tabs
                      v-model="tab"
                      background-color="deep-purple accent-4"
                      centered
                      dark
                      icons-and-text
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
                      hey
                      </v-tab-item>

                      <v-tab-item :value="'tab-' + 2">
                      2
                      </v-tab-item>

                      <v-tab-item :value="'tab-' + 3">
                      3
                      </v-tab-item>
                      </v-tabs>
              </v-column>
            </div>
          </v-row>





      </v-col>
    <v-col cols="4" style="background:blue;">Column</v-col>
  </v-row>
  </v-container>
</template>

<script>
export default {
data() {
  return {
    projects: [
      {seri:'C01',name:'SIKEN',user: '123300', bb: '1232200', pp: '2322200',tt: '2020', status:'Dealing'},
      {seri:'C02',name:'HONGLONG',user: '5200', bb: '1232200', pp: '2322200',tt: '2020', status:'Waiting'},
      {seri:'C03',name:'KUNHEAR',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'12'},
      {seri:'C04',name:'CHEA_C',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'Player Win'},
      {seri:'C05',name:'MAkara',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'Shuffling'},
      {seri:'C06',name:'HEAT_S',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'Waiting'},
      {seri:'C07',name:'SVEYNAR',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'12'},
      {seri:'C08',name:'CHANDA',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'Shuffling'},
      {seri:'C09',name:'YORNNEN',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'Dealing'},
      {seri:'C10',name:'PHALLA',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'Waiting'},

    ]
  }
}
}
</script>

<style scoped>
.dashboard-card {
  background:#120e09;
  height: 50px;
  margin-top: 5px;
}

</style>
