<!-- Vue Basics -->
<template>
  <v-container padding>
  <!-- Remove old code -->
  <input v-model="message"
  @keyup.esc="clearMessage()"
  @keyup.enter="alertMessage()"
  
  />
  <button @click="message=clearMessage()">Clear</button>
  <h5>{{ message }}</h5>


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

</style>



