<template>
  <v-container class="pa-0 ma-1" fluid>
    <!-- first row -->
      <v-row no-gutters dense>
        <dashboardCard v-for="room in roomList" :key="room.roomId" :room="room" :PropCardSize="PropCardSize"/>
      </v-row>


      
  </v-container>
</template>

<script>
import dashboardCard from '@/components/dashboardCard';

export default {
  components:{
    dashboardCard
  },
   computed: {
   
    PropCardSize() {
        let viewType= this.$route.params.viewType
        switch(viewType){
          case 'default':
            return 'md6';
          case 'road_map_view':
            return 'md4';
          case 'big_road_view':
            return 'md3';
          default:
            return 'md6'
        }
    },
   },
data() {
  return {
    roomList: [
      {roomId:'C01',name:'SIKEN',user: '123300', bb: '1232200', pp: '2322200',tt: '2020', status:'Dealing'},
      {roomId:'C02',name:'HONGLONG',user: '5200', bb: '1232200', pp: '2322200',tt: '2020', status:'Waiting'},
      {roomId:'C03',name:'KUNHEAR',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'12'},
      {roomId:'C04',name:'KUNHEAR1',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'12'},
      {roomId:'C05',name:'KUNHEAR2',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'12'},
      {roomId:'C06',name:'KUNHEAR3',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'12'},
      {roomId:'C07',name:'KUNHEAR4',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'12'},
      {roomId:'C08',name:'KUNHEAR5',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'12'},
      {roomId:'C09',name:'KUNHEAR6',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'12'},
      {roomId:'C010',name:'KUNHEAR7',user: '2200', bb: '1232200', pp: '2322200',tt: '2020', status:'12'},

    ]
  }
}
}
</script>

<style scoped>



</style>
