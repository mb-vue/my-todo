<!-- Vue Basics -->
<template>
  <v-container padding>
  <!-- Remove old code -->
  <input v-model="message"
  @keyup.esc="clearMessage()"
  @keyup.enter="alertMessage()"
 
  
  />
  <button @click="message=clearMessage()">Clear</button>
  <!-- <h5 class="border-grey" v-show="message.length">{{ message }}</h5> -->
  <!-- use v-if instead v-show-->
  <h5 class="border-grey" v-if="message.length">{{ message }}</h5>
  <!-- cnt cmd space to insert emoji-->
  <h3 v-else>No message entered 😎</h3>


  </v-container>
</template>

<!-- Remove old script -->

<script>
  export default {
    name: 'HelloWorld',

    // create data object return some data 
    data() {
      return {
        message: 'I love Jackie'
      }
    },
    methods: {
      clearMessage() {
        this.message=''
      },
      alertMessage() {
        alert(this.message)
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



