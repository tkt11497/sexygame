<template>
 <v-container class="pa-0 ml-1" fluid style="background-color:black">
   
   
  
<v-row class="pa-0" style="height:96vh;" no-gutters>
   <v-img v-show="showImage" width="3vw" height="3vw" contain :style="{ left: page.left+ 'vw', top: page.top+ 'px' ,position:'absolute','z-index':1000}" :src="'/coin/'+betCoin"/>
  <TutorialBetroom1 @close="tutorial=false" v-if="tutorial"/>
    <v-col class="pa-0" cols="7">
        <div class="playTable" id="v-step-0">
           <v-btn class="mx-2"  dark small color="#4F3C2B" style="position:absolute;bottom:1%;left:0" link to="/betRoom/betRoom2">
              <v-icon dark>picture_in_picture</v-icon>
            </v-btn>
            <v-btn class="mx-2"  dark small color="#4F3C2B" style="position:absolute;bottom:10%;right:0">
              <v-icon dark>switch_video</v-icon>
            </v-btn>
            <v-btn class="mx-2"  dark small color="#4F3C2B" style="position:absolute;bottom:1%;right:0">
              <v-icon dark>fullscreen</v-icon>
            </v-btn>
            <div class="room-title d-flex justify-center align-center white--text">
                    Baccrart C01
            </div>
              <v-avatar
                    color="rgba(0,0,0,0.5)"
                    size="130"
                    class="gameCountDown"
                    v-show="true">
                        <v-progress-circular
                        :value="70"
                        color="red"
                        size="100"
                        >
                    <span> 60</span>
                    </v-progress-circular>
                </v-avatar>
        </div>
       <!--beting play section-->
        <v-tabs
        background-color="#404040"
        class="elevation-2"
        centered
        grow
        dark
        height="4vh"
        hide-slider
        active-class="tabActive black--text" 
      >


              <v-tab
                :href="`#tab-1`"
                style="color:#F7D9AB;"

              >
               <span style="font-size:0.8vw"> Baccarat</span>
              </v-tab>
              <v-tab
                :href="`#tab-2`"
                style="color:#F7D9AB;"
              >
                <span style="font-size:0.8vw">  No Commission</span>
              </v-tab>
              <v-tab
                :href="`#tab-3`"
                style="color:#F7D9AB;"
              >
                <span style="font-size:0.8vw">  Cow Cow</span>
              </v-tab>

              <v-tab-item
                :value="'tab-' + 1"
              >
              <v-card
                  flat
                  tile
                  height="30vh" 
                  class="playArea" 
                   @mouseenter="showImage = true"
                       @mousemove="onMouseMove"
                        @mouseleave="showImage = false" 
                >
                <div class="d-flex justify-center align-center stopBetting" v-if="false">
                   
                  Stop Betting
                </div>
                <div class="d-flex flex-column justify-center align-center bettingSuccess" v-if="true">
                   <v-icon color="green" size="60">done</v-icon>
                   Betting Success
                </div>
                 
                  <v-row style="height:55%;width:100%; margin:0">
                    <v-col tile cols="4" class="playArea-tile" style="position:relative" align="center" @click="placeBet='player'">
                      <h1> Player</h1>
                        <h2>1:1</h2>
                         <v-img v-if="PlacedBets.some((item)=>item.bet=='player')" 
                         width="4vw" 
                         height="4vw" 
                         style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%)"
                          contain  
                          :src="'/coin/'+betCoin"/>
                        <div class="betConfirm" v-if="placeBet=='player'">
                          <v-img height="4vw" width="4vw" contain src="/coin/黑色籌碼.png"/>
                           <v-row justify="center">
                              <v-img src="/icon/萬用選擇UI.png"
                                            @click.stop="placeBet=null"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>

                                          <!-- </v-btn> -->
                                          <v-img src="/icon/萬用取消UI.png"
                                            @click.stop="confirmBet('player')"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>
                           </v-row>

                        </div>
                    </v-col>
                    <v-col tile cols="4" class="pa-0" align="center" >
                      <div class="tie tie1 playArea-tile " @click="placeBet='tie'" >
                        <h2> Tie</h2>
                        <h2>8:1</h2>
                         <v-img v-if="PlacedBets.some((item)=>item.bet=='tie')" 
                         width="4vw" 
                         height="4vw" 
                         style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%)"
                          contain  
                          :src="'/coin/'+betCoin"/>
                        <div class="betConfirm" v-if="placeBet=='tie'">
                          <v-img height="4vw" width="4vw" contain src="/coin/黑色籌碼.png"/>
                           <v-row justify="center">
                              <v-img src="/icon/萬用選擇UI.png"
                                            @click.stop="placeBet=null"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>

                                          <!-- </v-btn> -->
                                          <v-img src="/icon/萬用取消UI.png"
                                            @click.stop="confirmBet('tie')"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>
                           </v-row>

                        </div>
                      </div>
                      <div  class="tie playArea-tile " @click="placeBet='luckySix'">
                        <h2> Lucky Six</h2>
                        <h2> 12:1 / 20:1</h2>
                            <v-img v-if="PlacedBets.some((item)=>item.bet=='luckySix')" 
                         width="4vw" 
                         height="4vw" 
                         style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%)"
                          contain  
                          :src="'/coin/'+betCoin"/>
                        <div class="betConfirm" v-if="placeBet=='luckySix'">
                          <v-img height="4vw" width="4vw" contain src="/coin/黑色籌碼.png"/>
                           <v-row justify="center">
                              <v-img src="/icon/萬用選擇UI.png"
                                            @click.stop="placeBet=null"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>

                                          <!-- </v-btn> -->
                                          <v-img src="/icon/萬用取消UI.png"
                                            @click.stop="confirmBet('luckySix')"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>
                           </v-row>

                        </div>
                      </div>
                    </v-col>
                    <v-col tile cols="4" class="playArea-tile banker" align="center" @click="placeBet='banker'">
                      <h1> Banker</h1>
                        <h2>0.95:1</h2>
                         <v-img v-if="PlacedBets.some((item)=>item.bet=='banker')" 
                         width="4vw" 
                         height="4vw" 
                         style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%)"
                          contain  
                          :src="'/coin/'+betCoin"/>
                        <div class="betConfirm" v-if="placeBet=='banker'">
                          <v-img height="4vw" width="4vw" contain src="/coin/黑色籌碼.png"/>
                           <v-row justify="center">
                              <v-img src="/icon/萬用選擇UI.png"
                                            @click.stop="placeBet=null"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>

                                          <!-- </v-btn> -->
                                          <v-img src="/icon/萬用取消UI.png"
                                            @click.stop="confirmBet('banker')"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>
                           </v-row>

                        </div>
                    </v-col>
                  </v-row>
                  <v-row style="height:45%;width:100%; margin:0">
                    <v-col tile cols="3" class="playArea-tile1" align="center" @click="placeBet='pp'">
                        <h1>Player Pair</h1>
                        <h2>11:1</h2>
                          <v-img v-if="PlacedBets.some((item)=>item.bet=='pp')" 
                         width="4vw" 
                         height="4vw" 
                         style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%)"
                          contain  
                          :src="'/coin/'+betCoin"/>
                        <div class="betConfirm" v-if="placeBet=='pp'">
                          <v-img height="4vw" width="4vw" contain src="/coin/黑色籌碼.png"/>
                           <v-row justify="center">
                              <v-img src="/icon/萬用選擇UI.png"
                                            @click.stop="placeBet=null"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>

                                          <!-- </v-btn> -->
                                          <v-img src="/icon/萬用取消UI.png"
                                            @click.stop="confirmBet('pp')"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>
                           </v-row>

                        </div>
                    </v-col>
                    <v-col tile cols="3" class="playArea-tile1" align="center" @click="placeBet='pn'">
                        <h1>Player Natural</h1>
                        <h2>7:2</h2>
                         <v-img v-if="PlacedBets.some((item)=>item.bet=='pn')" 
                         width="4vw" 
                         height="4vw" 
                         style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%)"
                          contain  
                          :src="'/coin/'+betCoin"/>
                        <div class="betConfirm" v-if="placeBet=='pn'">
                          <v-img height="4vw" width="4vw" contain src="/coin/黑色籌碼.png"/>
                           <v-row justify="center">
                              <v-img src="/icon/萬用選擇UI.png"
                                            @click.stop="placeBet=null"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>

                                          <!-- </v-btn> -->
                                          <v-img src="/icon/萬用取消UI.png"
                                            @click.stop="confirmBet('pn')"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>
                           </v-row>

                        </div>
                    </v-col>
                    <v-col tile cols="3" class="playArea-tile1 banker" align="center" @click="placeBet='bn'">
                        <h1>Banker Natural</h1>
                        <h2>7:2</h2>
                         <v-img v-if="PlacedBets.some((item)=>item.bet=='bn')" 
                         width="4vw" 
                         height="4vw" 
                         style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%)"
                          contain  
                          :src="'/coin/'+betCoin"/>
                        <div class="betConfirm" v-if="placeBet=='bn'">
                          <v-img height="4vw" width="4vw" contain src="/coin/黑色籌碼.png"/>
                           <v-row justify="center">
                              <v-img src="/icon/萬用選擇UI.png"
                                            @click.stop="placeBet=null"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>

                                          <!-- </v-btn> -->
                                          <v-img src="/icon/萬用取消UI.png"
                                            @click.stop="confirmBet('bn')"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>
                           </v-row>

                        </div>
                    </v-col>
                    <v-col tile cols="3" class="playArea-tile1 banker" align="center" @click="placeBet='bp'">
                        <h1>Banker Pair</h1>
                        <h2>11:1</h2>
                         <v-img v-if="PlacedBets.some((item)=>item.bet=='bp')" 
                         width="4vw" 
                         height="4vw" 
                         style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%)"
                          contain  
                          :src="'/coin/'+betCoin"/>
                        <div class="betConfirm" v-if="placeBet=='bp'">
                          <v-img height="4vw" width="4vw" contain src="/coin/黑色籌碼.png"/>
                           <v-row justify="center">
                              <v-img src="/icon/萬用選擇UI.png"
                                            @click.stop="placeBet=null"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>

                                          <!-- </v-btn> -->
                                          <v-img src="/icon/萬用取消UI.png"
                                            @click.stop="confirmBet('bp')"
                                            class="ma-2"
                                            max-width="2vw"
                                            max-height="2vw"></v-img>
                           </v-row>

                        </div>
                    </v-col>
                  </v-row>
               
              </v-card>

              </v-tab-item>
                <v-tab-item
                :value="'tab-' + 2"
              >
              <v-card
                  flat
                  tile
                  height="30vh" 
                  class="playArea"
                >
                
                  <v-row style="height:55%;width:100%; margin:0">
                    <v-col tile cols="4" class="playArea-tile" align="center">
                      <h1> Player</h1>
                        <h2>1:1</h2>
                    </v-col>
                    <v-col tile cols="4" class="playArea-tile pa-0" align="center">
                      <div class="tie tie1">
                        <h2> Tie</h2>
                        <h2>8:1</h2>
                      </div>
                      <div  class="tie">
                        <h2> Lucky Six</h2>
                        <h2> 12:1 / 20:1</h2>
                      </div>
                    </v-col>
                    <v-col tile cols="4" class="playArea-tile banker" align="center">
                      <h1> Banker</h1>
                        <h2>1:1</h2>
                    </v-col>
                  </v-row>
                  <v-row style="height:45%;width:100%; margin:0">
                    <v-col tile cols="3" class="playArea-tile1" align="center">
                        <h1>Player Pair</h1>
                        <h2>11:1</h2>
                    </v-col>
                    <v-col tile cols="3" class="playArea-tile1" align="center">
                        <h1>Player Natural</h1>
                        <h2>7:2</h2>
                    </v-col>
                    <v-col tile cols="3" class="playArea-tile1 banker" align="center">
                        <h1>Banker Natural</h1>
                        <h2>7:2</h2>
                    </v-col>
                    <v-col tile cols="3" class="playArea-tile1 banker" align="center">
                        <h1>Banker Pair</h1>
                        <h2>11:1</h2>
                    </v-col>
                  </v-row>
               
              </v-card>
              </v-tab-item>
                <v-tab-item
                :value="'tab-' + 3"
              >
                <v-card
                  flat
                  tile
                  height="30vh" 
                  class="playArea"
                >
               
                    <v-row style="height:100%;width:100%; margin:0">
                        <v-col tile cols="4" class="playArea-tile" align="center">
                          <h1> Player</h1>
                            <h2>1:1</h2>
                        </v-col>
                        <v-col tile cols="4" class="playArea-tile" align="center">

                            <h2> Tie</h2>
                            <h2>8:1</h2>

                        </v-col>
                        <v-col tile cols="4" class="playArea-tile banker" align="center">
                          <h1> Banker</h1>
                            <h2>1:1</h2>
                        </v-col>
                  </v-row>
                
                </v-card>
              </v-tab-item>
      </v-tabs>
       <!--total bet amount-->
          <div
            style="height:4vh ;background-color:#023016;"
            class="d-flex justify-center align-center white--text"
            >
                Total BetAmount : 0.0

          </div>
        <!--betcoin selection-->
        <div class="selectCoin d-flex align-center white--text pa-2" >

                            <v-menu
                              offset-y
                              top
                              :close-on-content-click="false"
                              v-model="coinMenu"
                              :nudge-width="450"
                              :max-width="450"
                              dark
                              >
                                  <template v-slot:activator="{ on, attrs }">
                                                  <div class="text-center mt-1 mx-2"
                                                  style="width:2.7vw;
                                                   height:2.6vw;
                                                    background-image:url('/icon/七人座自定UI.png');
                                                    background-repeat: no-repeat;
                                                    background-position: center;
                                                    background-size: 100% 100%;"
                                                  v-bind="attrs"
                                                    v-on="on"
                                                    @click="openCoinSelect">


                                                  </div>
                                  </template>
                                  <v-card color='rgba(0, 0, 0, 0.7)' elevation="20">
                                    <v-card-title>
                                      <v-row no-gutters justify="center"> Please Select


                                      </v-row>
                                      </v-card-title>
                                      <v-row no-gutters justify="center">
                                          <v-img
                                                v-for="(coin,n) in coinList" :key="n"
                                                class="text-center ma-2"
                                                max-width="3.7vw"
                                                max-height="2.6vw"
                                                :src="'/coin/'+coin"
                                              >
                                                <v-checkbox v-model="selectedCoin"
                                                 :value="coin"
                                                 color="#009167"
                                                 :disabled="disableCoinSelect?selectedCoin.includes(coin)?false:true:false"
                                                 ></v-checkbox>
                                              </v-img>

                                      </v-row>
                                    <v-card-actions >
                                    <v-row justify="center">
                                      <!-- <v-btn small class="mx-2" fab dark color="#4f3c2b" @click="cancelCoinSelect"> -->

                                        <v-img src="/icon/萬用選擇UI.png"
                                        @click="cancelCoinSelect"
                                        class="ma-2"
                                        max-width="2.5vw"
                                        max-height="2.5vw"></v-img>

                                      <!-- </v-btn> -->
                                      <v-img src="/icon/萬用取消UI.png"
                                        @click="changeShowing"
                                        class="ma-2"
                                        max-width="2.5vw"
                                        max-height="2.5vw"></v-img>

                                    </v-row>
                                    </v-card-actions>
                                  </v-card>

                            </v-menu>
                            <v-img :src="betCoin==coin?'/coin/籌碼發光.png':''"
                                  @click="betCoin=coin"
                                  v-for="(coin,n) in showingCoin"
                                  :key="n"
                                  max-width='4.9vw'
                                  height='3.9vw'
                                  >

                                      <v-row
                                        class="fill-height ma-0"
                                        align="center"
                                        justify="center"
                                      >
                                        <v-img
                                              max-width="3.7vw"
                                              max-height="2.6vw"
                                              :src="'/coin/'+coin"


                                              >
                                        </v-img>
                                      </v-row>

                            </v-img>
                              <div class="text-center mt-1 ml-2"
                                                    style="width:2.7vw;
                                                    height:2.6vw;
                                                      background-image:url('/icon/單人雙倍ui.png');
                                                      background-repeat: no-repeat;
                                                      background-position: center;
                                                      background-size: 100% 100%">


                                </div>


        </div>
    </v-col>
    <!--betroom detail-->
    <v-col cols="5" class="pa-0">
     <BetRoom1Tableinfo />
  <v-row no-gutters>
    <v-col cols="9">
      <!--betroom history and other betrooms history-->
      <BetHistory />
    </v-col>
    <v-col cols="3">
      <BetRoom1SideTable  />

    </v-col>
  </v-row>



    </v-col>

</v-row>

      <button v-show="!drawer" class="Custombutton"  style="position:absolute; top:12vh;right:0;" @click="drawer=true" >
        <p class="py-5" style="writing-mode: vertical-rl;text-orientation: upright;letter-spacing:-2px;font-size:0.8vw">
          tables
        </p>
      </button>


  <TableDrawer :drawer="drawer"  @close="drawer=false"/>
 </v-container>

</template>

<script>
// import previewTable from '@/components/previewTable';
// import tableDrawer from '@/components/tableDrawer';
export default {
  // components:{
  //       previewTable,
  //       tableDrawer
  //   },
   mounted () {
      
    },
    computed:{
      disableCoinSelect(){
        if(this.selectedCoin.length==5){
          return true
        }else{
        return false
         }
      },

    },
  data () {
    return {
      PlacedBets:[],
      placeBet:'',
      page:{left: 170,top:0},
      showImage:false,
      tutorial:true,
      drawer:false,
      coinMenu:false,
      selectedCoin:[],
      showingCoin:['5籌碼.png','10K籌碼.png','10籌碼.png','20K籌碼.png','50籌碼.png'],
      coinList:['5籌碼.png','10K籌碼.png','10籌碼.png','20K籌碼.png','20籌碼.png','50籌碼.png','100籌碼.png',
                '200籌碼.png','500籌碼.png','1000籌碼.png','2000籌碼.png','5000籌碼.png'],
      betCoin:'5籌碼.png',
            }
            },
  methods:{
    confirmBet(bet){
      this.PlacedBets.push({bet:bet,amount:'50'})
      this.placeBet=''
    },
     onMouseMove(e) {
                console.log('page x: ',  e.pageX*100/window.screen.width, e.clientY);
                console.log(window.screen.width)
                this.page.left = (e.pageX*100/window.screen.width)-7;
                this.page.top = e.pageY;
            },
      changeShowing(){
          this.showingCoin=[...this.selectedCoin]
          this.coinMenu=false
        },
      openCoinSelect(){
        this.selectedCoin=[...this.showingCoin]
      },
      cancelCoinSelect(){
        this.selectedCoin=[]
        this.coinMenu=false
      }
  }
}
</script>
<style scoped>
.betConfirm{
  position:absolute; 
  width:100%;
  height:100%;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  z-index: 20;
}
  .stopBetting{
    font-size:0.8vw;
    width:20%;
    height:30%;
    background-color:rgba(0,0,0,0.5);
    position:absolute;
    color:white;
    top:50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 20;
  }
    .bettingSuccess{
    font-size:0.9vw;
    width:25%;
    height:35%;
    background-color:rgba(0,0,0,0.5);
    position:absolute;
    color:green;
    top:50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 20;
  }
 .scroll {
      overflow-y: auto;
    }
    .playTable{
        background-image: url("/icon/荷官暫代圖.png");
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 50%;
        position: relative;
    }
    .playArea-tile{
        border:1px solid rgba(255,255,255, 0.3);
        color:#3470A9;
        font-size:1.2vw ;
        position: relative;
    }
    .playArea-tile:hover {
        background-color: #0E541B;
    }
    .playArea-tile1:hover {
        background-color: #0E541B;
    }
     .playArea-tile1{
        border:1px solid rgba(255,255,255, 0.3);
        color:#3470A9;
        font-size:0.7vw ;
        position: relative;
    }
    .player{
      color:#3470A9
    }
    .banker{
      color:red
    }
    .tie-text{
      color:#0C930A;
    }
    .tie{
      height:50%;
      width:100%;
      margin:0;
      color:#0C930A;
       font-size:0.75vw ;
    }
    .tie1{
      border-bottom: 1px solid  rgba(255,255,255, 0.3);
    }
    .playArea{
        background-color:rgb(3, 62, 29);
        /* width:100%;
        height:100%; */
        /* cursor: url('/21.png') 2 2,auto; */
        position: relative;
    }
    .selectCoin{
        width: 100%;
        background-color:black
    }
    .table-info{
      font-size: 0.8vw;
    }
    .room-list{
        font-size: 0.8vw;
    }
    .room-title{
        width:20%;
        height:5vh;
        position:absolute;
        top:0;
        left:0;
        background-color:rgba(0,0,0,0.5);
        font-size: 1vw;
    }
    .gameCountDown{
        position:absolute;
        top:10%;
        left:5%;
    }
    .tabActive{
      background-image:
      linear-gradient(
          rgb(255, 255, 255) 63%,
          #B98F38
        );

    }
    .Custombutton {
      border: none;
      color: white;
      padding: 9px;
      text-align: center;
      text-decoration: none;
      display: inline-block;
      font-size: 0.8vw;
      margin: 0px 8.5px;
      cursor: pointer;
      background-image:url('/icon/選擇桌台ui_1.png');
      background-repeat: no-repeat;
      background-position: center;
      background-size: 100% 100%;
      letter-spacing:20px;

    }
    .Custombutton:focus {
    outline: 1px solid #F7D8A8;
    outline-offset: -4px;
}

</style>
