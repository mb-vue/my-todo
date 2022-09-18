<!-- Vue Basics -->
<template>
  <v-container padding>
  <!-- Remove old code -->
  <input v-model="message"/>
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
    }
  }
</script>

<!-- Add style here -->

<style>

</style>



