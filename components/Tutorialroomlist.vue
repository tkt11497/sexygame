<template>
    <div style="width:100%;height:100%;background-color:rgba(0,0,0,0.8);position:absolute;z-index:20">
        
   </div>
</template>
<script>
export default {
    data(){
        return{
            step:1
        }
    },
    methods:{
        close(){
            this.$emit('close')
        },
        goNext(current){
            if(current>3){
                this.close()
            }else
            {
                this.step=current
            }
            
        }
    }
}
</script>
<style scoped>
.hr{
    width:17vw;
    height:2px;border-width:0;
    color:#F7D9AB;
    background-color:#F7D9AB;
    position: absolute;
}
.hr2{
     left:50%;
    top:46vh
}
.step1row1{
    height:19%;
    width:100%;
     margin:0;
     background-color:black;
     position:absolute;
     bottom:5%;
}
.step1row2{
    height:5%;
    width:100%; 
    margin:0; 
    background-color:#876F4D;
    position:absolute;
    bottom:0
}
    .dot {
        height: 10px;
        width: 10px;
        background-color: #F7D9AB;
        border-radius: 50%;
        display: inline-block;
        position: absolute;
        }
    .dot1 {
        left:49.55%;
        top:46vh
    }
    .dot2 {
        left:49.8%;
        top:35vh
    }
.step1card{
     position: absolute;
        left:50%;
        transform: translate(-50%);
        top:47vh
}
.step2card{
     position: absolute;
        left:50%;
        transform: translate(-50%);
        top:20vh;
}
.vl {
  border-left: 2px solid #F7D9AB;
  height: 10vh;
  position: absolute;
}
.vl1{
     left:50%;
    top:36vh
}
.vl2{
     left:50%;
    top:36vh;
    
}
.outLine{
    height:24%;
    width:100%; 
    margin:0;
    background-color:rgba(0,0,0,0);
    position:absolute;
    bottom:0;
    outline:3px solid #F7D9AB;
    outline-offset:1px
}
.table-info{
      font-size: 0.8vw;
    }
</style>