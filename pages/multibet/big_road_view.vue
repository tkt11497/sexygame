<template>
  <v-container class=" ml-2" fluid>
    <v-row >
      <!-- Main First Col -->
      <v-col cols="8" style="padding:0;" >

            <v-tabs
              fixed-tabs
              background-color=#1c170e
              dark
              active-class="brown darken-4 text--accent-4"
            >
              <v-tab href="#navtab-1" style="color:#b5a182;border-right:3px solid black;" v-if="favoriteshow">
                  My favorite
              </v-tab>
              <v-tab href="#navtab-2">
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



              <!-- <v-row>
                <v-col cols="3">card1</v-col>
                <v-col cols="3">card2</v-col>
                <v-col cols="3">card3</v-col>
                <v-col cols="3">card4</v-col>
              </v-row> -->
        <v-tab-item :value="'navtab-' + 2">
          <v-row style="width:100%;" class="pa-0" no-gutters>

            <multibetBigRoad v-for="project in projects" :key="project.name" :project="project">

            </multibetBigRoad>

          </v-row>

        </v-tab-item>
          </v-tabs>
      </v-col>
<!-- End Main First Col -->


<!-- Main Second Col -->
    <v-col  cols="4" style="padding:0;">
        <multibetSlite></multibetSlite>

    </v-col>
<!-- End Main Second Col -->
  </v-row>
  </v-container>
</template>

<script>
import multibetSlite from '@/components/multibet/multibet1';
import multibetBigRoad from '@/components/multibet/multibetBigRoad';
export default {
  components:{
    multibetSlite,
    multibetBigRoad
  },
data() {
  return {
    betLimit:'10-1000',
    favoriteshow: false,
    projects: [
      {seri:'C01',name:'SIKEN',user: '12', bb: '12', pp: '23',tt: '220', status:'Dealing'},
      {seri:'C02',name:'HONGLONG',user: '52', bb: '123', pp: '20',tt: '220', status:'Waiting'},
      {seri:'C03',name:'KUNHEAR',user: '20', bb: '12', pp: '230',tt: '2020', status:'12'},
      {seri:'C04',name:'CHEA_C',user: '22', bb: '12', pp: '232',tt: '220', status:'Player Win'},
      {seri:'C05',name:'MAkara',user: '22', bb: '123', pp: '230',tt: '220', status:'Shuffling'},
      {seri:'C06',name:'HEAT_S',user: '220', bb: '123', pp: '230',tt: '220', status:'Waiting'},
      {seri:'C07',name:'SVEYNAR',user: '22', bb: '123', pp: '230',tt: '220', status:'12'},
      {seri:'C08',name:'CHANDA',user: '220', bb: '120', pp: '2',tt: '202', status:'Shuffling'},
      {seri:'C09',name:'YORNNEN',user: '22', bb: '123', pp: '20',tt: '220', status:'Dealing'},
      {seri:'C10',name:'PHALLA',user: '22', bb: '200', pp: '230',tt: '200', status:'Waiting'},

    ],
    changenumbers: {
      '10-1000':{bet_limit:'10 - 1,000', banker:'1,000', player:'1,000', tie:'125', pair:'90'},
      '50-5000':{bet_limit:'50 - 5,000', banker:'5,000', player:'5,000', tie:'625', pair:'454'},
      '100-5000':{bet_limit:'100 - 5,000', banker:'5,000', player:'5,000', tie:'625', pair:'454'},
      '100-10k':{bet_limit:'100 - 10K', banker:'10,000', player:'10,000', tie:'1250', pair:'909'},
      '200-20k':{bet_limit:'200 - 20K', banker:'20,000', player:'20,000', tie:'2500', pair:'1818'},
    },

    headers: [
        {
          text: 'Table',
          align: 'start',

        },
        { text: 'Bet Content', value: 'category' },
        { text: 'Bet Amount', value: 'bet_amount' },
        { text: 'Win/Lose', value: 'winlose' },
        { text: 'Remark', value: 'remark' },
      ],
      desserts: [
        {
          name: '',
          category: '',
          bet_amount:'',

        },
        {
          name: '',
          category: '',
        },
        {
          name: '',
          category: '',
        },
        {
          name: '',
          category: '',
        },
        {
          name: '',
          category: '',
        },
        {
          name: '',
          category: '',
        },
        {
          name: '',
          category: '',
        },

        {
          name: '',
          category: '',
        },
      ],

  }
}
}
</script>

<style scoped>

.playTable{
    background-image: url("/table.png");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 300px;
    margin: 0;
    padding: 0;
}
.changepicture {
  background-color: #231b12;
  height: 9vh;
  width: 100%;
  margin-top:0.1vh;
}



</style>
