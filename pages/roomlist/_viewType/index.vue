<template>
  <v-container class="pa-0 ml-2 mt-0 viewList" fluid>
    <!-- first row -->
      <v-row no-gutters dense >
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
.viewList{
  overflow-y: auto;
  overflow-x: hidden;
  height: 96vh;
  background-color:#444444;
  width:100%;
}
.viewList::-webkit-scrollbar {
    width: 13px;
}
 
/* Track */
.viewList::-webkit-scrollbar-track {
    -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3); 
    -webkit-border-radius: 10px;
    border-radius: 10px;
    background: rgba(245, 223, 178, 0.2);
}
 
/* Handle */
.viewList::-webkit-scrollbar-thumb {
    -webkit-border-radius: 10px;
    border-radius: 10px;
    background:#AA8647; 
    /* -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,1);  */
}


</style>
