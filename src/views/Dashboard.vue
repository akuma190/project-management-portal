<template>
  <div class="dashboard">
   <h1 class="subheading grey--text">Dashboard</h1>

    <v-container class="my-5">

      <v-card-flat class="pa3">
        <v-layout row wrap class="pink lighten-5 "> 
        <v-flex xs12 md6>
          <div class="caption grey--text">Project Title</div>
          <div>Vue JS Portal</div>
        </v-flex>
         <v-flex xs6 sm4 md2>
          <div class="caption grey--text">Person</div>
          <div>Ashish Kumar</div>
        </v-flex>
         <v-flex xs6 sm4 md2>
          <div class="caption grey--text">Due By:</div>
          <div>1st Jan 2020</div>
        </v-flex>
         <v-flex xs2 sm4 md2>
          <div class="caption grey--text">Status</div>
          <div>Ongoing</div>
        </v-flex>
      </v-layout>

      </v-card-flat>
      

    </v-container>


  </div>
</template>

<script>
// @ is an alias to /src


export default {
 
}
</script>
