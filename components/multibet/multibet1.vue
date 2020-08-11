<template>
  <div>
  <div class="playTable">

  </div>
<!-- start slite -->
<div style="width:100%;background:white">

<v-sheet
  class="mx-auto "
  elevation="8"

>
  <v-slide-group style="background:#e5e8e7;"
  >
    <v-row style="height:13vh;">
      <v-row style="width:100%;">
       <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 ml-13"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text pa-5">C01</span>

      </v-card>
    </v-slide-item>

        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">C02</span>

      </v-card>
    </v-slide-item>

        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">C03</span>

      </v-card>
    </v-slide-item>

        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">C04</span>

      </v-card>
    </v-slide-item>

        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 ml-10"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">P03</span>

      </v-card>
    </v-slide-item>

        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">P04</span>

      </v-card>
    </v-slide-item>

        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">P05</span>

      </v-card>
    </v-slide-item>

        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 m-15"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">P06</span>

      </v-card>
    </v-slide-item>

        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 ml-10"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A03</span>

      </v-card>
    </v-slide-item>

        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A04</span>

      </v-card>
    </v-slide-item>
        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A05</span>

      </v-card>
    </v-slide-item>
        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A06</span>

      </v-card>
    </v-slide-item>
        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 ml-10"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A11</span>

      </v-card>
    </v-slide-item>
        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 "
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A12</span>

      </v-card>
    </v-slide-item>
        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 "
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">CD &T</span>

      </v-card>
    </v-slide-item>
        <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 "
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">P D&T</span>

      </v-card>
    </v-slide-item>
    </v-row>
    <v-row >
      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 ml-13"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">C05</span>

      </v-card>
    </v-slide-item>

      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">C06</span>

      </v-card>
    </v-slide-item>

      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">P01</span>

      </v-card>
    </v-slide-item>

      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">P02</span>

      </v-card>
    </v-slide-item>

      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 ml-10"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">P07</span>

      </v-card>
    </v-slide-item>

      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">P08</span>

      </v-card>
    </v-slide-item>

      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A01</span>

      </v-card>
    </v-slide-item>

      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A02</span>

      </v-card>
    </v-slide-item>

      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 ml-10"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A07</span>

      </v-card>
    </v-slide-item>
      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4 ml-"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A08</span>

      </v-card>
    </v-slide-item>
      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A09</span>

      </v-card>
    </v-slide-item>
      <v-slide-item

      v-slot:default="{ active, toggle }"
    >
      <v-card
        :color="active ? '#b98f38' : '#404040'"
        class="ma-4"
        height="30"
        width="80"
        @click="toggle"
         align="center"
      ><span class="white--text ">A10</span>

      </v-card>
    </v-slide-item>
    </v-row>
    </v-row>
  </v-slide-group>
</v-sheet>


</div>
<!-- End slite -->

<v-row>
<span class="subtitle-2 text-center pa-2 mt-2  white--text " style="background:#aa8647; width:100%"><h3>Bet Information</h3></span>
</v-row>

  <v-data-table
  :headers="headers"
  :items="desserts"
  :items-per-page="8"
  disable-sort
  dense
  orange



  item-key="name"
  class="elevation-1"
  :footer-props="{
    showFirstLastPage: true,


    firstIcon: 'mdi-arrow-collapse-left',
    lastIcon: 'mdi-arrow-collapse-right',
    prevIcon: 'mdi-minus',
    nextIcon: 'mdi-plus'
  }"
></v-data-table>

<div class="changenumber" >
  <v-layout >

      <v-flex class="ml-3 mt-4">
        <span style="font-size:18px;">Bet-Limit</span><br>
        <span class="black--text">{{ changenumbers[betLimit].bet_limit }}</span>
      </v-flex>
        <v-flex class="mr-2 mt-4">
          <span style="font-size:18px;">Banker</span><br>
          <span class="black--text">{{ changenumbers[betLimit].banker }}</span>
        </v-flex>
        <v-flex class="mr-2 mt-4">
          <span style="font-size:18px;">Player</span><br>
          <span class="black--text">{{ changenumbers[betLimit].player }}</span>
        </v-flex>
        <v-flex class="mr-2 mt-4">
          <span style="font-size:18px;">Tie</span><br>
          <span class="black--text">{{ changenumbers[betLimit].tie }}</span>
        </v-flex>
        <v-flex class="mr-2 mt-4">
          <span style="font-size:18px;">Pair</span><br>
          <span class="black--text">{{ changenumbers[betLimit].pair}}</span>
        </v-flex>
        <v-flex class=" mt-5">
          <div class="d-flex justify-center">
            <v-menu
            offset-y
            top
            close-on-content-click
            :nudge-width="100"
            left
            :max-width="250"
            >
        <template v-slot:activator="{ on, attrs }">
           <v-btn
           icon
           class="pa-2 ma-1 mr-5"
           v-bind="attrs"
            v-on="on"
           >
              <v-btn color=#c3a66e class="white--text ">Change</v-btn>
            </v-btn>
        </template>


         <v-card>
              <v-list
              dark

              color="rgba(12, 10, 6, 0.8)">

              <v-radio-group v-model="betLimit" :mandatory="false">
                <v-radio label="10 - 1,000" value='10-1000' on-icon="done" off-icon="" ></v-radio>
                <v-radio label="50 - 5,000" value='50-5000' on-icon="done" off-icon="" ></v-radio>
                <v-radio label="100 - 5,000" value='100-5000' on-icon="done" off-icon=""></v-radio>
                <v-radio label="100 - 10K" value='100-10k' on-icon="done" off-icon=""></v-radio>
                <v-radio label="200 - 20K" value='200-20k' on-icon="done" off-icon=""></v-radio>
              </v-radio-group>

          </v-list>
        </v-card>
      </v-menu>
          </div>
        </v-flex>


  </v-layout>

  <v-layout style="background:#1c1c1c; width:100%">
      <v-flex class=" mt-3">
        <v-btn

color="#4c4331"
class="ma-2 white--text"
@click="loader = 'loading3'"
><v-icon left dark>monetization_on</v-icon>
Custom

</v-btn>
      </v-flex>
      <v-flex class=" mt-4">
        <img src="/coin/5籌碼.png" style="width:3.2vw;" />
      </v-flex>
        <v-flex class=" mt-4">
          <img src="/coin/10籌碼.png" style="width:3.2vw;" />
        </v-flex>
        <v-flex class=" mt-4">
          <img src="/coin/20籌碼.png" style="width:3.2vw;" />
        </v-flex>
        <v-flex class=" mt-4">
          <img src="/coin/50籌碼.png" style="width:3.2vw;" />
        </v-flex>
        <v-flex class=" mt-4">
          <img src="/coin/100籌碼.png" style="width:3.2vw;" />
        </v-flex>



  </v-layout>
</div>
</div>
</template>

<style scoped>
.playTable{
    background-image: url("/icon/荷官暫代圖.png");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 33.2vh;
    margin: 0;
    padding: 0;
}
</style>

<script>

export default {
  components:{
   
  },
data() {
  return {
    betLimit:'10-1000',
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
      changenumbers: {
        '10-1000':{bet_limit:'10 - 1,000', banker:'1,000', player:'1,000', tie:'125', pair:'90'},
        '50-5000':{bet_limit:'50 - 5,000', banker:'5,000', player:'5,000', tie:'625', pair:'454'},
        '100-5000':{bet_limit:'100 - 5,000', banker:'5,000', player:'5,000', tie:'625', pair:'454'},
        '100-10k':{bet_limit:'100 - 10K', banker:'10,000', player:'10,000', tie:'1250', pair:'909'},
        '200-20k':{bet_limit:'200 - 20K', banker:'20,000', player:'20,000', tie:'2500', pair:'1818'},
      },
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
