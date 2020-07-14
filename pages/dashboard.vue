<template>
  <v-container >
    <v-row>
      <v-col>
        <v-card v-if="project.name === 'siken'" flat v-for="project in projects" :key="project.name" >
          <v-layout >
            <v-flex>
              <div>Seri {{ project.seri}} </div>
            </v-flex>
              <v-flex >
                <div><v-icon>group</v-icon> {{ project.user}} </div>
              </v-flex>
                  <v-flex>
                    <v-avatar color="red" size="25">
                      <span class="white--text">B</span>
                    </v-avatar>
                    <span>{{project.bb}}</span>
                  </v-flex>
                    <v-flex>
                      <v-avatar color="blue" size="25">
                        <span class="white--text ">P</span>
                    </v-avatar>
                        <span>{{project.pp}}</span>
                    </v-flex>
                          <v-flex>
                            <div >
                              <v-avatar color="red" size="25">
                                <span class="white--text">T</span>
                              </v-avatar>
                              {{project.tt}}
                            </div>
                          </v-flex>
                          <v-flex>
                                <div style="background:#196260; height:30px;">
                                  <div> {{project.status}} </div>
                                </div>
                          </v-flex>
                </v-layout>
            </v-card>



      <v-row>
          <div>
            <v-img
              height="200"
              width="150"
              src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
            ></v-img>
          </div>

          <div style="border: 1px solid gray; width:650px; height:200px;">

          </div>
      </v-row>
  </v-col>

 <!-- Second Card -->
  <v-col>
    <v-card v-if="project.name === 'siken'" flat v-for="project in projects" :key="project.name" >
      <v-layout >
        <v-flex>
          <div>Seri {{ project.seri}} </div>
        </v-flex>
          <v-flex >
            <div><v-icon>group</v-icon> {{ project.user}} </div>
          </v-flex>
              <v-flex>
                <v-avatar color="red" size="25">
                  <span class="white--text">B</span>
                </v-avatar>
                <span>{{project.bb}}</span>
              </v-flex>
                <v-flex>
                  <v-avatar color="blue" size="25">
                    <span class="white--text ">P</span>
                </v-avatar>
                    <span>{{project.pp}}</span>
                </v-flex>
                      <v-flex>
                        <div >
                          <v-avatar color="red" size="25">
                            <span class="white--text">T</span>
                          </v-avatar>
                          {{project.tt}}
                        </div>
                      </v-flex>
                      <v-flex>
                            <div style="background:#196260; height:30px;">
                              <div> {{project.status}} </div>
                            </div>
                      </v-flex>
            </v-layout>
        </v-card>



  <v-row>
      <div>
        <v-img
          height="200"
          width="150"
          src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
        ></v-img>
      </div>

      <div style="border: 1px solid gray; width:650px; height:200px;">

      </div>
  </v-row>
</v-col>
<!-- End Second Card -->
    </v-row>

  </v-container>
</template>

<script>


export default {
data() {
  return {
    projects: [
      {seri:'C01',name:'siken',user: '123300', bb: '1232200', pp: '2322200',tt: '2020', status:'ongoing'},
      {seri:'C01',name:'honglang',user: '5200', bb: '1232200', pp: '2322200',tt: '2020', status:'complete'},
      {seri:'C01',name:'kunhear',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'overdue'},

    ]
  }
}
}
</script>

<style>


</style>
