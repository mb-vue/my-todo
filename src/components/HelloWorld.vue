<!-- Vue Basics -->
<template>
  <v-container padding>
  <!-- Remove old code -->
  <input v-model="message"/>
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
      }
    }
  }
</script>

<!-- Add style here -->

<style>

</style>



