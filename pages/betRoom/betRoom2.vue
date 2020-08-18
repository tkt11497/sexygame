<template>
 <v-container class="pa-0 ml-1" fluid>
<v-row class="pa-0" style="height:100vh;" no-gutters>
    <v-col cols="12">
        <div class="tableInfo">
                <div class="room-title d-flex justify-center align-center">
                    Baccrart C01
                </div>
                 <v-btn class="mx-2"  dark small color="#4F3C2B" style="position:absolute;bottom:1%;left:0" link to="/betRoom">
                    <v-icon dark>picture_in_picture</v-icon>
                </v-btn>
                <v-avatar
                    color="rgba(0,0,0,0.5)"
                    size="130"
                    class="gameCountDown"
                    v-show="false">
                        <v-progress-circular
                        :value="70"
                        color="red"
                        size="100"
                        >
                    <span> 60</span>
                    </v-progress-circular>
                </v-avatar>
                <div class="result-cards">
                     <v-img 
                    src="/card/方塊2.png" 
                    height="10vh" 
                    contain 
                     style="position:absolute;left:10%;top:1%; transform: rotate(-90deg);"/>
                    <v-img 
                    src="/card/方塊2.png" 
                    height="10vh" 
                    contain  
                     style=" position:absolute;left:0;bottom:18%"/>
                     <v-img 
                    src="/card/方塊2.png" 
                    height="10vh" 
                    contain
                     style=" position:absolute;left:19%;bottom:18%"/>
                    <div 
                    class=" d-flex justify-center align-center"
                    style="width:42%; height:10%; position:absolute; top:85%; left:5%; background-color:blue"> 
                        <span>P 6</span>
                    </div>
                      <v-img 
                    src="/card/方塊2.png" 
                    contain
                    height="10vh" 
                     style="position:absolute;right:10%;top:2%; transform: rotate(-90deg);"/>
                    <v-img 
                    src="/card/方塊2.png" 
                    contain
                    height="10vh" 
                     style=" position:absolute;right:0;bottom:18%"/>
                     <v-img 
                    src="/card/方塊2.png" 
                    contain
                    height="10vh" 
                     style="position:absolute;right:19%;bottom:18%"/>
                    <div 
                    class=" d-flex justify-center align-center"
                    style="width:42%; height:10%; position:absolute; top:85%; right:5%; background-color:red"> 
                        <span>B 5</span>
                    </div>
                </div>
              <BetRoom2Tableinfo/>


        </div>
        <v-row
        style="height:20vh;width:100%"
        class="pa-0 ma-0"
        >
         <BetHistory2/>
          <v-row no-gutters style="height:100%;  width:50%">
              <ResultBar/>
              <BetRoom2SideTable/>
              <Chat/>
          </v-row>
        </v-row>

    </v-col>
    <!-- <v-col cols="2"></v-col> -->
      <button v-show="!drawer" class="Custombutton"  style="position:absolute; top:37vh;right:0" @click="drawer=true" >
        <p class="py-5" style="writing-mode: vertical-rl;text-orientation: upright;letter-spacing:-2px;font-size:0.8vw">
          tables
        </p>
      </button>
      <TableDrawer :drawer="drawer"  @close="drawer=false"/>
</v-row>

 </v-container>
</template>

<script>
// import previewTable from '@/components/PreviewTable';
export default {
  // components:{
  //       previewTable
  //   },
  data () {
    return {
      drawer:false
            }
            }
}
</script>
<style scoped>
 .scroll {
      overflow-y: auto;
    }
    .tableInfo{
        background-image: url("/table.png");
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 75%;
        position: relative;
    }
    .playArea-tile{
        border:1px solid rgba(255,255,255, 0.3);
        color:#3470A9;
        font-size:1.2vw ;
    }
     .playArea-tile1{
        border:1px solid rgba(255,255,255, 0.3);
        color:#3470A9;
        font-size:0.7vw ;
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

    .selectCoin{
        width: 100%;
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
        color:white
    }
    .gameCountDown{
        position:absolute;
        top:10%;
        left:5%;
    }
    .result-cards{
        background-color:rgba(46, 46, 46, 0.6);
         position:absolute;
          top:5vh;
          left:0;
        width:20%;
        height:23vh
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
