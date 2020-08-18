<template>
  <div class="emoji-picker" >
    <v-card height="300px" >
      <v-card-title class="blue white--text">
        <span class="headline">Emoji Picker</span>
      </v-card-title>
      <v-card-text>
        <div class="emoji-content">
            <span v-for="emoji in emojis"  :key="emoji.key" @click="onEmojiClick">{{emoji.character}}</span>
        </div>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
 
  import axios from 'axios'
  export default {
    data () {
      return {
        emojis: ['\ud83d\ude00','\ud83d\ude00']
      }
    },
    created () {
      axios.get('https://emoji-api.com/categories/travel-places?access_key=5e527e740e326870e7546b1230a45a2b9f6674d6').then(response => {
        console.log(response)
        this.emojis = response.data
      }).catch((e) => { console.log(e) })
    },
    methods: {
      onEmojiClick (emoji) {
        this.$emit('click', emoji)
      },
      closePicker () {
        this.$emit('close')
      }
    },

  }
</script>

<style scoped>
  .emoji-picker{
    background: white;
    position: absolute;
    bottom: 5rem;
    left: 0;
    width: 200px;
    user-select: none;
  }
  .emoji-picker .emoji-header{
    display: flex;
    padding: 5px;
    box-shadow: 0px 5px 9px 0px rgba(0,0,0,0.15);
  }

  .emoji-picker .emoji-header .emoji-close{
    margin-left: auto;
  }
  .emoji-picker .emoji-content{
    margin-top: 10px;
    overflow-y: auto;
    height: 200px;
  }
  .emoji-picker span{
    cursor: pointer;
    font-size: 25px;
  }
</style>
