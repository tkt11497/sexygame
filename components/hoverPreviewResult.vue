 <template>
    <v-tooltip top color="rgb(255,255,255,0)">
      <template v-slot:activator="{ on, attrs }" >
        <v-avatar color="indigo" size="16" 
        v-bind="attrs"
          v-on="on">
          <span class="white--text" style="font-size:0.5vw">P</span>
        </v-avatar>
      </template>
      <v-card height="200" width="300" >
        <v-row no-gutters class="pa-1" >
          <v-col cols="6">
            ID 10234512312
          </v-col>
          <v-col cols="6">
            Round 4-1
          </v-col>
        </v-row>
        <v-divider/>
        <v-row no-gutters justify="center">
          Click roadmap to replay
        </v-row>
              <div class="result-cards"> 
                    
                    <div 
                    class=" d-flex justify-center align-center"
                    style="width:42%; height:10%; position:absolute; top:5%; left:5%; background-color:blue"> 
                        <span>Player 8</span>
                    </div>
                      
                    <div 
                    class=" d-flex justify-center align-center"
                    style="width:42%; height:10%; position:absolute; top:5%; right:5%; background-color:red"> 
                        <span>Banker 0</span>
                    </div>
                        <img 
                    src="/hovercard.png" 
                     style="width:15%; height:23%; position:absolute;left:27%;top:20%"/>
                       <img 
                    src="/hovercard.png" 
                     style="width:15%; height:23%; position:absolute;left:10%;top:20%"/>
                       <img 
                    src="/hovercard.png" 
                     style="width:15%; height:23%; position:absolute;right:27%;top:20%"/>
                       <img 
                    src="/hovercard.png" 
                     style="width:15%; height:23%; position:absolute;right:10%;top:20%"/>
                      <div 
                    class=" d-flex justify-center align-center"
                    style="width:42%; 
                            height:10%;  
                            position: absolute;
                              bottom:5%;
                              left: 50%;
                              transform: translate(-50%, -50%); background-color:blue"> 
                        <span>Player Win</span>
                    </div>
                </div>
      </v-card>
    </v-tooltip>
</template>

<script>
export default {

}
</script>

<style scoped>
        .result-cards{
        background-color:rgba(0, 0, 0, 0.5);
         position: relative;;
        width:100%; 
        height:100%
    }
</style>

