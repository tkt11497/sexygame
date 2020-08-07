 <template>       
        <v-flex :md4="cardSize.md4" :md3="cardSize.md3" :md6="cardSize.md6" xs12>
          <v-card class="ma-2" elevation="24" raised outlined>
            <v-row no-gutters class="dashboard-bar" v-if="PropCardSize=='md6'">
                  <v-flex row class=" align-center">
                    <span class="black--text textSize ml-4">Seri {{project.seri}}  </span>
                  </v-flex>
                    <v-flex row class="align-center" >
                      <v-icon color="#B98F38">group</v-icon>  
                      <span class="black--text textSize">{{project.user}} </span>
                    </v-flex>
                        <v-flex row class="align-center">
                          <v-img  src="/icon/圓庄.png" max-height="1vw" max-width="1vw">
                          </v-img>
                          <span class="black--text textSize">{{project.bb}}</span>
                        </v-flex>
                          <v-flex row class="align-center">
                            <v-img  src="/icon/圓閒.png" max-height="1vw" max-width="1vw">
                            </v-img>
                              <span class="black--text textSize">{{project.pp}}</span> 
                          </v-flex>
                                <v-flex row class="align-center">
                                 
                                    <v-img  src="/icon/圓和.png" max-height="1vw" max-width="1vw">
                                   </v-img>
                                   <span class="black--text textSize"> {{project.tt}}</span>
                                  
                                </v-flex>
                                <v-flex >
                                      <div class="white--text textSize text-center" style="background:#404040; height:30px;">
                                        <span> {{project.status }}</span>
                                      </div>
                                </v-flex>
            </v-row >
            <v-row no-gutters class="dashboard-bar" v-if="PropCardSize!='md6'">
               <v-flex row class=" align-center">
                    <span class="black--text textSize ml-4">Seri {{project.seri}}  </span>
                  </v-flex>
                    <v-flex row class="align-center" >
                      <v-icon color="#B98F38">group</v-icon>  
                      <span class="black--text textSize">{{project.user}} </span>
                    </v-flex>
                        <v-flex row class="align-center">
                          <v-img  src="/icon/圓庄.png" max-height="1vw" max-width="1vw">
                          </v-img>
                          <span class="black--text textSize">{{project.bb}}</span>
                        </v-flex>
            </v-row >
            <v-row no-gutters class="dashboard-bar" v-if="PropCardSize!='md6'">
              <v-flex row class="align-center ml-1">
                            <v-img  src="/icon/圓閒.png" max-height="1vw" max-width="1vw">
                            </v-img>
                              <span class="black--text textSize">{{project.pp}}</span> 
                          </v-flex>
                                <v-flex row class="align-center">
                                 
                                    <v-img  src="/icon/圓和.png" max-height="1vw" max-width="1vw">
                                   </v-img>
                                   <span class="black--text textSize"> {{project.tt}}</span>
                                  
                                </v-flex>
                                <v-flex >
                                      <div class="white--text textSize text-center" style="background:#404040; height:30px;">
                                        <span> {{project.status }}</span>
                                      </div>
                                </v-flex>
            </v-row>
                  <v-row no-gutters dense>
                        <div :style="{height:PropCardSize=='md3'?'12vh':'21vh', width:'17%'}">
                          <v-img
                            height="100%"
                            width="100%"
                            src="/icon/荷官頭圖.png"
                          ></v-img>
                        </div>
                          <v-hover v-slot:default="{ hover }">
                    <!-- Start show resultimg -->
                      <div class="showing-resulting" :style="{height:PropCardSize=='md3'?'12vh':'21vh'}">
                         <div :style="{width:'100%', height:'100%', 
                          'background-image': 'url(\'/icon/'+ 
                          `${PropCardSize=='md6'?'珠盤路單(大).png':PropCardSize=='md4'?'檯桌棋盤格.png':'珠盤路單(小).png'}`
                          + '\')',
                          'background-repeat': 'no-repeat',
                          'background-position': 'center',
                          'background-size': '100% 100%'}">
                             <v-row no-gutters style="height:100%">
                                    <div 
                                      :style="{height:'100%', width:PropCardSize=='md3'?'100%':'39%',}"
                                      class="d-flex align-content-start flex-wrap"
                                          v-if="PropCardSize=='md6'||PropCardSize=='md3'">
                                        <!-- <previewTable :row="7" :column="15" /> -->
                                         <v-img class="my-1" src="/icon/圓庄.png" :max-height="PropCardSize=='md3'?'0.8vw':'1.2vw'" :max-width="PropCardSize=='md3'?'0.75vw':'1.3vw'">
                                         </v-img>
                                         <v-img class="my-1" src="/icon/圓閒.png" :max-height="PropCardSize=='md3'?'0.8vw':'1.2vw'" :max-width="PropCardSize=='md3'?'0.75vw':'1.3vw'">
                                         </v-img>
                                         <v-img class="my-1" src="/icon/圓庄.png" :max-height="PropCardSize=='md3'?'0.8vw':'1.2vw'" :max-width="PropCardSize=='md3'?'0.75vw':'1.3vw'">
                                         </v-img>
                                         <v-img class="my-1" src="/icon/圓閒.png" :max-height="PropCardSize=='md3'?'0.8vw':'1.2vw'" :max-width="PropCardSize=='md3'?'0.75vw':'1.3vw'">
                                         </v-img>
                                          <v-img class="my-1"  src="/icon/圓庄.png" :max-height="PropCardSize=='md3'?'0.8vw':'1.2vw'" :max-width="PropCardSize=='md3'?'0.75vw':'1.3vw'">
                                         </v-img>
                                          
                                        
                                    </div>
                                    <div :style="{ height: '100%', width: PropCardSize=='md4'?'100%':'60%', }" 
                                    v-if="PropCardSize=='md4'||PropCardSize=='md6'">
                                        <div style="width:100%; height:49%;">
                                                <!-- <previewTable :row="6" :column="36"/> -->
                                            </div>
                                            <div style="width:100%; height:26.5%;">
                                                <!-- <previewTable :row="3" :column="36"/> -->
                                            </div>
                                           
                                        <v-row style="width:100%; height:24.5%" no-gutters>
                                            <div style="width:50%; height:100%; ">
                                            <!-- <previewTable :row="4" :column="18"/> background-color:rgba(0, 0, 102,0.5)-->
                                            </div>
                                            
                                            <div style="width:50%; height:100%;">
                                                <!-- <previewTable :row="4" :column="18"/> -->
                                            </div>
                                        </v-row>
                                    </div>
                             </v-row>
                         </div>
                    <!-- first button -->
                    <div 
                      v-if="hover&&!show &&!secondshow"
                      class="d-flex align-center v-card--reveal justify-center #1f180e darken-2 display-3 white--text"

                      style="height: 100%; background:black;"
                    >
                    <!-- <v-input v-model="show">{{show}}</v-input> -->

                        <div class=" mr-5 ">
                            <v-btn class="white--text" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35"  @click="show=true">Baccarat</v-btn>
                        </div>

                        <div class="mr-5 " >
                            <v-btn class="white--text" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35" @click="secondshow=true">7-Seat Baccarat</v-btn>
                        </div>


                    </div>
                    <!-- end first button -->


                      <!-- first button- second action-->
                      <div
                        v-if="hover ? show&& hover : show=false "
                        class=" #1f180e darken-2 v-card--reveal display-3 white--text"

                        style="height: 100%; background:gray;"
                      >
                        <div class="d-flex align-center flex-row justify-center">
                            <v-btn class="white--text mt-9 mr-3" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35" link to="/betRoom">10 - 1,000</v-btn>



                            <v-btn class="white--text mt-9 mr-3" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35" link to="/betRoom">50 - 5,000</v-btn>


                            <v-btn class="white--text mt-9 mr-3" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35" link to="/betRoom">100 - 5,000</v-btn>
                          </div>

                          <div class="d-flex align-center flex-row justify-center">

                            <v-btn class="white--text mt-4 mr-3" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35" link to="/betRoom">100 - 5,000</v-btn>


                            <v-btn class="white--text mt-4 mr-3" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35" link to="/betRoom">100 - 5,000</v-btn>
                          </div>
                       

                      </div>
                      <!-- end first button- second action-->



                      <!-- second button- second action-->
                      <div
                        v-if="hover ? secondshow&& hover : secondshow=false "
                        class=" #1f180e darken-2 v-card--reveal display-3 white--text"

                        style="height: 100%; background:gray;"
                      >
                        <div class="d-flex align-center flex-row justify-center">
                            <v-btn class="white--text mt-9 mr-3" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35" link to="/betRoom">10 - 1,000</v-btn>



                            <v-btn class="white--text mt-9 mr-3" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35" link to="/betRoom">50 - 5,000</v-btn>


                            <v-btn class="white--text mt-9 mr-3" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35" link to="/betRoom">100 - 5,000</v-btn>
                          </div>

                          <div class="d-flex align-center flex-row justify-center">

                            <v-btn class="white--text mt-4 mr-3" link to="/betRoom" :small="PropCardSize=='md3'"  :large="!PropCardSize=='md3'" depressed color="#5f4d35">100 - 5,000</v-btn>


                            <v-btn class="white--text mt-4 mr-3" :small="PropCardSize=='md3'" :large="!PropCardSize=='md3'" depressed color="#5f4d35" link to="/betRoom">100 - 5,000</v-btn>
                          </div>

                      </div>
                      <!-- end second button- second action-->

                      </div>
                      <!-- End show resultimg -->
                      </v-hover>
                    </v-row>
            
        </v-card>
        </v-flex>
</template>
<script>
import previewTable from './previewTable';
export default {
    props:['project','PropCardSize'],
      components:{
        previewTable
    },
    data() {
      
    return {
        show: false,
        secondshow: false,
        
    }
   },
   computed: {
   
    cardSize() {
       switch(this.PropCardSize){
         case 'md6':
          return {
          md6:true,
          md4:false,
          md3:false
        }
        break;
        case 'md4':
          return {
          md6:false,
          md4:true,
          md3:false
        }
        break;
        case 'md3':
          return {
            md6:false,
            md4:false,
            md3:true
          }
        break;
        default:
          return {
          md6:true,
          md4:false,
          md3:false
        }

       }
        
    }
  },

}
</script>
<style scoped>
.v-card--reveal {

bottom: 0;

opacity: 0.6;
position: absolute;
width: 100%;
}
.dashboard-bar{
  background-image:
  linear-gradient(
      rgb(255, 255, 255) 63%, 
      #B98F38
    );
  color:black;
}
.showing-resulting {
   width:83%;
   height:21vh;
   margin: 0;
   padding: 0;
   position: relative;
}
.profile-img {
  margin-left:11px;
}
.textSize{
  font-size: 0.8vw;
}


</style>