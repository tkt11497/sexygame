<template>
  <v-container >
    <!-- first row -->
    <v-row>

        <v-col>
          <v-card v-if="project.name === 'SIKEN'" flat v-for="project in projects" :key="project.name" >
            <div class="dashboard-card">
              <v-layout>
                <v-flex>
                  <span class="white--text">Seri {{ project.seri}}</span>
                </v-flex>
                  <v-flex >
                    <div class="white--text"><v-icon class="white--text">group</v-icon> {{ project.user}} </div>
                  </v-flex>
                      <v-flex>
                        <v-avatar color="red" size="25">
                          <span class="white--text">B</span>
                        </v-avatar>
                        <span class="white--text">{{project.bb}}</span>
                      </v-flex>
                        <v-flex>
                          <v-avatar color="blue" size="25">
                            <span class="white--text ">P</span>
                        </v-avatar>
                            <span class="white--text">{{project.pp}}</span>
                        </v-flex>
                              <v-flex>
                                <div class="white--text">
                                  <v-avatar color="red" size="25">
                                    <span class="white--text">T</span>
                                  </v-avatar>
                                  {{project.tt}}
                                </div>
                              </v-flex>
                              <v-flex>
                                    <div class="white--text" style="background:#196260; height:30px;">
                                      <div> {{project.status}} </div>
                                    </div>
                              </v-flex>
                    </v-layout>
            </div>
        </v-card>


              <v-row>
                  <div class="profile-img" >
                    <v-img
                      height="200"
                      width="150"
                      src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
                    ></v-img>
                  </div>

                  <v-hover v-slot:default="{ hover }">
                      <div class="showing-resultimg"  >

                      <div :class="`justify-center justify-xl-center`"
                        v-if="hover&&!show"
                        class="d-flex  #1f180e darken-2 v-card--reveal display-3 white--text"

                        style="height: 100%; background:gray;"
                      >
                      <!-- <v-input v-model="show">{{show}}</v-input> -->

                      <div class="mt-15 mr-5 ">
                          <v-btn class="white--text" large depressed color="#5f4d35"  @click="show=true">Primary</v-btn>
                      </div>

                      <div class="mt-15 mr-5 " >
                          <v-btn class="white--text"  large depressed color="#5f4d35">Secondary</v-btn>
                      </div>


                      </div>

                      <div :class="`justify-center justify-xl-center`"
                        v-if="hover ? show&& hover : show=false "
                        class="d-flex  #1f180e darken-2 v-card--reveal display-3 white--text"

                        style="height: 100%; background:gray;"
                      >
                      <!-- <v-input v-model="show">{{show}}</v-input> -->

                      <div class="mt-15 mr-5 ">
                          <v-btn class="white--text" large depressed color="#5f4d35"  @click="show = true">sadsadsadsa</v-btn>
                      </div>

                      <div class="mt-15 mr-5 " >
                          <v-btn class="white--text"  large depressed color="#5f4d35">Secondary</v-btn>
                      </div>


                      </div>

                      </div>
                      </v-hover>
              </v-row>
    </v-col>


    <!-- first row - second column -->
    <v-col>
      <v-card v-if="project.name === 'HONGLONG'" flat v-for="project in projects" :key="project.name" >
        <div class="dashboard-card">
          <v-layout>
            <v-flex>
              <span class="white--text">Seri {{ project.seri}}</span>
            </v-flex>
              <v-flex >
                <div class="white--text"><v-icon class="white--text">group</v-icon> {{ project.user}} </div>
              </v-flex>
                  <v-flex>
                    <v-avatar color="red" size="25">
                      <span class="white--text">B</span>
                    </v-avatar>
                    <span class="white--text">{{project.bb}}</span>
                  </v-flex>
                    <v-flex>
                      <v-avatar color="blue" size="25">
                        <span class="white--text ">P</span>
                    </v-avatar>
                        <span class="white--text">{{project.pp}}</span>
                    </v-flex>
                          <v-flex>
                            <div class="white--text">
                              <v-avatar color="red" size="25">
                                <span class="white--text">T</span>
                              </v-avatar>
                              {{project.tt}}
                            </div>
                          </v-flex>
                          <v-flex>
                                <div class="white--text" style="background:#196260; height:30px;">
                                  <div> {{project.status}} </div>
                                </div>
                          </v-flex>
                </v-layout>
        </div>
    </v-card>


          <v-row>
              <div class="profile-img">
                <v-img
                  height="200"
                  width="150"
                  src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
                ></v-img>
              </div>

              <div class="showing-resultimg">

              </div>
          </v-row>
   </v-col>
   <!-- end first row - second column -->
    </v-row>
<!-- End first row -->



<!-- second row -->
<v-row>

    <v-col>
      <v-card v-if="project.name === 'KUNHEAR'" flat v-for="project in projects" :key="project.name" >
        <div class="dashboard-card">
          <v-layout>
            <v-flex>
              <span class="white--text">Seri {{ project.seri}}</span>
            </v-flex>
              <v-flex >
                <div class="white--text"><v-icon class="white--text">group</v-icon> {{ project.user}} </div>
              </v-flex>
                  <v-flex>
                    <v-avatar color="red" size="25">
                      <span class="white--text">B</span>
                    </v-avatar>
                    <span class="white--text">{{project.bb}}</span>
                  </v-flex>
                    <v-flex>
                      <v-avatar color="blue" size="25">
                        <span class="white--text ">P</span>
                    </v-avatar>
                        <span class="white--text">{{project.pp}}</span>
                    </v-flex>
                          <v-flex>
                            <div class="white--text">
                              <v-avatar color="red" size="25">
                                <span class="white--text">T</span>
                              </v-avatar>
                              {{project.tt}}
                            </div>
                          </v-flex>
                          <v-flex>
                                <div class="white--text" style="background:#196260; height:30px;">
                                  <div> {{project.status}} </div>
                                </div>
                          </v-flex>
                </v-layout>
        </div>
    </v-card>


          <v-row>
              <div class="profile-img">
                <v-img
                  height="200"
                  width="150"
                  src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
                ></v-img>
              </div>

              <div class="showing-resultimg">

              </div>
          </v-row>
</v-col>


<!-- second row - second column -->
<v-col>
  <v-card v-if="project.name === 'CHEA_C'" flat v-for="project in projects" :key="project.name" >
    <div class="dashboard-card">
      <v-layout>
        <v-flex>
          <span class="white--text">Seri {{ project.seri}}</span>
        </v-flex>
          <v-flex >
            <div class="white--text"><v-icon class="white--text">group</v-icon> {{ project.user}} </div>
          </v-flex>
              <v-flex>
                <v-avatar color="red" size="25">
                  <span class="white--text">B</span>
                </v-avatar>
                <span class="white--text">{{project.bb}}</span>
              </v-flex>
                <v-flex>
                  <v-avatar color="blue" size="25">
                    <span class="white--text ">P</span>
                </v-avatar>
                    <span class="white--text">{{project.pp}}</span>
                </v-flex>
                      <v-flex>
                        <div class="white--text">
                          <v-avatar color="red" size="25">
                            <span class="white--text">T</span>
                          </v-avatar>
                          {{project.tt}}
                        </div>
                      </v-flex>
                      <v-flex>
                            <div class="white--text" style="background:#196260; height:30px;">
                              <div> {{project.status}} </div>
                            </div>
                      </v-flex>
            </v-layout>
    </div>
</v-card>


      <v-row>
          <div class="profile-img">
            <v-img
              height="200"
              width="150"
              src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
            ></v-img>
          </div>

          <div class="showing-resultimg">

          </div>
      </v-row>
</v-col>
<!-- end second row - second column -->
</v-row>
<!-- End second row -->



<!-- third row -->
<v-row>

    <v-col>
      <v-card v-if="project.name === 'KUNHEAR'" flat v-for="project in projects" :key="project.name" >
        <div class="dashboard-card">
          <v-layout>
            <v-flex>
              <span class="white--text">Seri {{ project.seri}}</span>
            </v-flex>
              <v-flex >
                <div class="white--text"><v-icon class="white--text">group</v-icon> {{ project.user}} </div>
              </v-flex>
                  <v-flex>
                    <v-avatar color="red" size="25">
                      <span class="white--text">B</span>
                    </v-avatar>
                    <span class="white--text">{{project.bb}}</span>
                  </v-flex>
                    <v-flex>
                      <v-avatar color="blue" size="25">
                        <span class="white--text ">P</span>
                    </v-avatar>
                        <span class="white--text">{{project.pp}}</span>
                    </v-flex>
                          <v-flex>
                            <div class="white--text">
                              <v-avatar color="red" size="25">
                                <span class="white--text">T</span>
                              </v-avatar>
                              {{project.tt}}
                            </div>
                          </v-flex>
                          <v-flex>
                                <div class="white--text" style="background:#196260; height:30px;">
                                  <div> {{project.status}} </div>
                                </div>
                          </v-flex>
                </v-layout>
        </div>
    </v-card>


          <v-row>
              <div class="profile-img">
                <v-img
                  height="200"
                  width="150"
                  src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
                ></v-img>
              </div>

              <div class="showing-resultimg">

              </div>
          </v-row>
</v-col>


<!-- third row - second column -->
<v-col>
  <v-card v-if="project.name === 'CHEA_C'" flat v-for="project in projects" :key="project.name" >
    <div class="dashboard-card">
      <v-layout>
        <v-flex>
          <span class="white--text">Seri {{ project.seri}}</span>
        </v-flex>
          <v-flex >
            <div class="white--text"><v-icon class="white--text">group</v-icon> {{ project.user}} </div>
          </v-flex>
              <v-flex>
                <v-avatar color="red" size="25">
                  <span class="white--text">B</span>
                </v-avatar>
                <span class="white--text">{{project.bb}}</span>
              </v-flex>
                <v-flex>
                  <v-avatar color="blue" size="25">
                    <span class="white--text ">P</span>
                </v-avatar>
                    <span class="white--text">{{project.pp}}</span>
                </v-flex>
                      <v-flex>
                        <div class="white--text">
                          <v-avatar color="red" size="25">
                            <span class="white--text">T</span>
                          </v-avatar>
                          {{project.tt}}
                        </div>
                      </v-flex>
                      <v-flex>
                            <div class="white--text" style="background:#196260; height:30px;">
                              <div> {{project.status}} </div>
                            </div>
                      </v-flex>
            </v-layout>
    </div>
</v-card>


      <v-row>
          <div class="profile-img">
            <v-img
              height="200"
              width="150"
              src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
            ></v-img>
          </div>

          <div class="showing-resultimg">

          </div>
      </v-row>
</v-col>
<!-- end second row - second column -->
</v-row>
<!-- End third row -->




<!-- fourth row -->
<v-row>

    <v-col>
      <v-card v-if="project.name === 'MAkara'" flat v-for="project in projects" :key="project.name" >
        <div class="dashboard-card">
          <v-layout>
            <v-flex>
              <span class="white--text">Seri {{ project.seri}}</span>
            </v-flex>
              <v-flex >
                <div class="white--text"><v-icon class="white--text">group</v-icon> {{ project.user}} </div>
              </v-flex>
                  <v-flex>
                    <v-avatar color="red" size="25">
                      <span class="white--text">B</span>
                    </v-avatar>
                    <span class="white--text">{{project.bb}}</span>
                  </v-flex>
                    <v-flex>
                      <v-avatar color="blue" size="25">
                        <span class="white--text ">P</span>
                    </v-avatar>
                        <span class="white--text">{{project.pp}}</span>
                    </v-flex>
                          <v-flex>
                            <div class="white--text">
                              <v-avatar color="red" size="25">
                                <span class="white--text">T</span>
                              </v-avatar>
                              {{project.tt}}
                            </div>
                          </v-flex>
                          <v-flex>
                                <div class="white--text" style="background:#196260; height:30px;">
                                  <div> {{project.status}} </div>
                                </div>
                          </v-flex>
                </v-layout>
        </div>
    </v-card>


          <v-row>
              <div class="profile-img">
                <v-img
                  height="200"
                  width="150"
                  src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
                ></v-img>
              </div>

              <div class="showing-resultimg">

              </div>
          </v-row>
</v-col>


<!-- fourth row - second column -->
<v-col>
  <v-card v-if="project.name === 'HEAT_S'" flat v-for="project in projects" :key="project.name" >
    <div class="dashboard-card">
      <v-layout>
        <v-flex>
          <span class="white--text">Seri {{ project.seri}}</span>
        </v-flex>
          <v-flex >
            <div class="white--text"><v-icon class="white--text">group</v-icon> {{ project.user}} </div>
          </v-flex>
              <v-flex>
                <v-avatar color="red" size="25">
                  <span class="white--text">B</span>
                </v-avatar>
                <span class="white--text">{{project.bb}}</span>
              </v-flex>
                <v-flex>
                  <v-avatar color="blue" size="25">
                    <span class="white--text ">P</span>
                </v-avatar>
                    <span class="white--text">{{project.pp}}</span>
                </v-flex>
                      <v-flex>
                        <div class="white--text">
                          <v-avatar color="red" size="25">
                            <span class="white--text">T</span>
                          </v-avatar>
                          {{project.tt}}
                        </div>
                      </v-flex>
                      <v-flex>
                            <div class="white--text" style="background:#196260; height:30px;">
                              <div> {{project.status}} </div>
                            </div>
                      </v-flex>
            </v-layout>
    </div>
</v-card>


      <v-row>
          <div class="profile-img">
            <v-img
              height="200"
              width="150"
              src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
            ></v-img>
          </div>

          <div class="showing-resultimg">

          </div>
      </v-row>
</v-col>
<!-- end fourth row - second column -->
</v-row>
<!-- End fourth row -->




  </v-container>
</template>

<script>


export default {
data() {
  return {
    show: false,
    projects: [
      {seri:'C01',name:'SIKEN',user: '123300', bb: '1232200', pp: '2322200',tt: '2020', status:'ongoing'},
      {seri:'C02',name:'HONGLONG',user: '5200', bb: '1232200', pp: '2322200',tt: '2020', status:'complete'},
      {seri:'C03',name:'KUNHEAR',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'overdue'},
      {seri:'C04',name:'CHEA_C',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'overdue'},
      {seri:'C05',name:'MAkara',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'overdue'},
      {seri:'C06',name:'HEAT_S',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'overdue'},
      {seri:'C07',name:'SVEYNAR',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'overdue'},
      {seri:'C08',name:'CHANDA',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'overdue'},
      {seri:'C09',name:'YORNNEN',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'overdue'},
      {seri:'C10',name:'PHALLA',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'overdue'},

    ]
  }
}
}
</script>

<style scoped>
.dashboard-card {
  background:#1f180e;
  width: 770px;
}
.showing-resultimg {
 border: 1px solid gray;
 width:620px;
 height:200px;
}
.profile-img {
margin-left:11px;
}


</style>
