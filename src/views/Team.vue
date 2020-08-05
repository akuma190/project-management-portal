<template>
  <div class="team">
   <h1 class="subheading grey--text">Team</h1>
    <v-container class="my-5">
     <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
          <v-card flat class="text-xs-center ma-3">
            <v-responsive class="pt-4">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="person.avatar">
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn flat color="grey">
                <v-icon small left>mdi-home</v-icon>
                <span class="">Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
   
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  data() {
    return {
      team: [
        { name: 'MS DHONI', role: 'Wicket Keeper', avatar: '/image1.png' },
        { name: 'Yuvraj Singh', role: 'SouthPaw', avatar: '/image2.png' },
        { name: 'Suresh raina', role: 'Flying Fielder' , avatar: '/image3.png'},
        { name: 'Rahul Dravid', role: 'The wall' , avatar: '/image4.png'},
        { name: 'Zaheer Khan', role: 'Reverse Swing', avatar: '/image5.png'}
      ]
    }
  }
}
</script>
