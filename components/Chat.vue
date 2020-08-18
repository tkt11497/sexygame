<template>
  
    <v-row no-gutters style="width:60%; height:100%">
      
        <div class="chat-container"  >
              <div class="message" v-for="(message,index) in messages" v-bind:key="index" :class="{own: message.user == 'mgmg'}">
                <span class="username">{{message.user}}</span>:
                <div class="content">
                  <div v-html="message.content"></div>
                  
                </div>
              </div>
        </div>
          
        <v-row  no-gutters class="typer" align="center">
           <v-col cols="1">
           <v-menu
                  offset-y
                  top
                  close-on-content-click
                  :nudge-width="100"
                  right
                  :max-width="250" 
                  >
              <template v-slot:activator="{ on, attrs }">
                 <v-btn 
                 icon 
                 class="white--text" 
                 v-bind="attrs"
                  v-on="on">
                    <v-icon>mdi-emoticon-outline</v-icon>
                  </v-btn>
              </template>


                
                  <v-card height="300px" class="emoji-picker" color="rgba(0,0,0,0.8)" >
                     <v-card-subtitle class="pl-2 pb-0 pt-1 white--text" style="background-color:#AA8647">Emojis</v-card-subtitle>
                    <v-card-text class="emoji-content">
                      
                          <span v-for="emoji in emojis"  :key="emoji.key" @click="addEmoji(emoji.character)">{{emoji.character}}</span>
                      
                    </v-card-text>
                  </v-card>
               
          </v-menu>
           </v-col>
          
          <v-col cols="9">
              <!-- <v-text-field
                label="Type Here" 
                style="font-size:0.8vw" 
                color="#AA8647"
                solo
                dense 
                flat 
                clearable 
                v-model="content"  
                v-on:keyup.enter="sendMessage"
              ></v-text-field> -->
              <input type="text" placeholder="Type here..." v-on:keyup.enter="sendMessage" v-model="content">
            
          </v-col>
          <v-col cols="2">
            <v-row no-gutters>
             <div class="sendButton d-flex justify-center">
                    <v-icon>arrow_drop_up</v-icon>
             </div>
             <div class="sendletter d-flex justify-center align-center">
                    Send
             </div>
            </v-row>
          
          </v-col>
        </v-row>
      
    </v-row>
 
</template>

<script>
  
 import axios from 'axios'
  export default {
    data () {
      return {
        content: '',
        messages: [{content:'do',date:'aad',user:'mgmg'},{content:'a lr',date:'aad',user:'a'},{content:'lsad',date:'aad',user:'b'},
        {content:'do',date:'aad',user:'mgmg'},{content:'do',date:'aad',user:'mgmg'}],
        emojis: ['\ud83d\ude00','\ud83d\ude00']
      }
    },
    created () {
      axios.get('https://emoji-api.com/categories/travel-places?access_key=5e527e740e326870e7546b1230a45a2b9f6674d6').then(response => {
        console.log(response)
        this.emojis = response.data
      }).catch((e) => { console.log(e) })
    },
    computed: {
     
    },
    watch: {
   
    },
    methods: {
      addEmoji(emoji){
        this.content=this.content+emoji

      },

    }
  }
</script>

<style scoped>
  .scrollable {
    overflow-y: auto;
    height: 90vh;
  }
  .typer{
    height: 21%;
    width: 100%;
    background-color: #AA8647; 
    font-size: 0.8vw;
  }
   .typer input[type=text]{
    width: 100%; 
    padding: 4px;
    background-color: white;
    border: none;
    outline: none;
    border-radius: 5px;
    font-size: 1vw;
  }
  .chat-container{
    box-sizing: border-box;
    height: 75%; 
    width:100%;
    overflow-y: auto;
    padding: 10px;
    background-color: #f2f2f2;
  }
  .message{
    margin-bottom: 3px;
  }
  .message.own{
    text-align: right;
  }
  .message.own .content{
    background-color: #E9E9E9;
  }
  .chat-container .username{
    font-size: 1vw;
    font-weight: bold;
  }
  .chat-container .content{
    padding: 4px;
    background-color:#E9E9E9;
    border-radius: 5px;
    display:inline-block;
    box-shadow: 0 1px 3px 0 rgba(0,0,0,0.2), 0 1px 1px 0 rgba(0,0,0,0.14), 0 2px 1px -1px rgba(0,0,0,0.12);
    max-width: 50%;
    word-wrap: break-word;
    font-size: 0.8vw;
    }
    /* span.emoji {
    font-size: 0.8vw;
    vertical-align: middle;
    line-height: 2;
  } */
   .emoji-picker span{
    cursor: pointer;
    font-size: 1vw;
    color:white
  }
   .emoji-picker .emoji-content{
    margin-top: 10px;
    overflow-y: auto;
    height: 220px;
  }
  .sendButton{
    width:50%;
    height:3.4vh; 
    background-color:#AA8647;
    box-shadow: 2px 2px 0px 0px rgba(0,0,0,0.3);
    cursor: pointer;
  }
  .sendletter{
    width:50%;
    height:3.4vh; 
    background-color:white; 
    color:black;
    box-shadow: 2px 2px 0px 0px rgba(0,0,0,0.3);
    cursor: pointer;
  }

</style>