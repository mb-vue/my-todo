<!-- Vue Basics -->
<template>
  <v-container padding>
  <!-- Remove old code -->

  <!--add counter-->
 
  <input v-model="message"
  @keyup.esc="clearMessage()"
  @keyup.enter="alertMessage()"
 
  
  />
  <button @click="message=clearMessage()">Clear</button>
   <button
    style="position: absolute; right: 10px; background-color: blue; color:white; width: 50px"
    @click="counter++"
  >{{ counter }}</button>
  <!-- <h5 class="border-grey" v-show="message.length">{{ message }}</h5> -->
  <!-- use v-if instead v-show-->
  <h5 class="border-grey" v-if="message.length">{{ message }}</h5>
  <!-- cnt cmd space to insert emoji-->
  <h3 v-else>No message entered 😎</h3>
  <hr>
  <p>Uppercase message: {{ messageUppercase() }}</p>




  </v-container>
</template>

<!-- Remove old script -->

<script>
  export default {
    name: 'HelloWorld',

    // create data object return some data 
    data() {
      return {
        message: 'I love Jackie',
        counter:0
      }
    },
    methods: {
      clearMessage() {
        this.message=''
      },
      alertMessage() {
        alert(this.message)
      },
      messageUppercase() {
        console.log("This message is firing everytime I click button");
        return this.message.toUpperCase()
      }

     
      }

    }
  
</script>

<!-- Add style here -->

<style>
  .border-grey {
    border: 2px solid grey;
  }
</style>



