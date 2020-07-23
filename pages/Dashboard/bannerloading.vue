<template>
<div class="container pt-14">
  <v-row align="center" justify="center" class="pa-6">
    <v-img
      src="https://bad.src/not/valid"
      lazy-src="https://picsum.photos/id/11/100/60"
      aspect-ratio="1"
      class="grey lighten-2"
      max-width="700"
      max-height="500"
    >
      <template v-slot:placeholder>
        <v-row
          class="fill-height ma-0"
          align="center"
          justify="center"
        >
          <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
        </v-row>
      </template>
    </v-img>
  </v-row>
  <div> {{ percent }}%</div>
    <div class="loading-bar">
      <div class="percentage" :style="{'width' : percentage + '%'}">

      </div>
    </div>
</div>
</template>

<script>
//import image from "./assets/banner_img.png"
export default {
  data: () => {
    return {
      percentage: 0
    }
  },
computed: {
    percent() {
      return this.percentage.toFixed();
    }
  },
  created() {
    var intval = setInterval(() => {
        if(this.percentage < 100)
        this.percentage += .1;
        else
          clearInterval(intval);
    },10);
  }
}
</script>

<style lang="scss" scoped>

.container {
  text-align: center;
  font-size: 20px;
  color: white;
  background: black;

}
.loading-bar {
  position: relative;
  margin: auto;
  width: 300px;
  height: 13px;
  border-radius: 15px;
  overflow: hidden;
  background-color: #808080;
  border-bottom: 1px solid gray;
  //box-shadow: inset 0 1px 4px rgba($color: #000, $alpha: .4),
            //0 -1px 1px #808080, 0 1px 0 #808080;


.percentage {
  position: absolute;
  top: 1px; left: 1px; right: 1px;
  display: block;
  height: 100%;
  border-radius: 15px;
  background-color: #ffff99;
  background-size: 30px 30px;
  background-image: linear-gradient(135deg, rgba($color: #fff, $alpha: .15) 25%, transparent 25%,
                    transparent 50%, rgba($color: #fff, $alpha: .15) 50%,
                    rgba($color: #fff, $alpha: .15) 75%, transparent 75%,
                    transparent);
  animation: animate-stripes 3s linear infinite;
  }
}

@keyframes animate-stripes {
  0% {background-position: 0 0;}
  100% {background-position: 60px 0;}
}

</style>
