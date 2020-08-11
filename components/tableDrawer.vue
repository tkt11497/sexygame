<template>
    <v-navigation-drawer
      dark 
      absolute
      right 
      floating 
      color="rgba(0,0,0,0)" 
      height="90vh" 
      width="30vw"
      style="top:2%" 
      v-model="drawer"
    >
        <v-row no-gutters style="width:100%;height:100%">
            <v-col cols="1" style="height:100%;">
                <v-row align="center" style="width:100%;height:100%;" no-gutters>
                <button class="Custombutton" @click="close" ><p class="py-5" style="writing-mode: vertical-rl;
            text-orientation: upright;letter-spacing:-2px; font-size:0.8vw">table</p></button>
                </v-row>

            </v-col>
            <v-col cols="11">
                <v-card style="
                    border:2px solid #BB9953; 
                    border-radius: 10px;" 
                    height="100%" 
                    color="rgba(0,0,0,0.6)">
                    <v-row style="height:10%;width:100%;" no-gutters></v-row>
                    <v-row style="height:90%;width:100%;" no-gutters>
                        <v-col cols="3">
                            <div class="d-flex flex-column justify-center align-center" style="width:100%;height:100%;">
                                <v-card height="2vw" width="5vw" 
                                    v-for="n in 7" 
                                    :key="n" 
                                    color="#404040" 
                                    style=" border:1px solid #BB9953; 
                                            border-radius: 5px; 
                                            font-size:0.8vw"  
                                    dark 
                                    class="d-flex justify-center align-center room-list mb-3" 
                                    @click="window=n" 
                                    :class="{ 'windowActive': window==n }">window {{n}}
                                </v-card>
                    
                            </div>
                        </v-col>
                        <v-col cols="9"></v-col>
                    </v-row>
                </v-card>
            </v-col>
        </v-row>
    </v-navigation-drawer> 
</template>
<script>
export default {
     props:['drawer'],
  components:{
      
    },
    computed:{
       
    },
  data () {
    return {
    }
            },
  methods:{
      close(){
          this.$emit('close')
      }
  }
}
</script>
<style scoped>
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
      background-image:url('/icon/選擇桌台ui_2.png');
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