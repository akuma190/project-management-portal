<template>
    <nav>
        <v-toolbar flat app>
            <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="tex-uppercase grey--text">
            <span class="font-weight-light">Project</span>
            <span>Mangement</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>

            <!-- dropdown menu -->
      <v-menu offset-y>
        <v-btn flat slot="activator" color="grey">
          <v-icon left>mdi-home</v-icon>
          <span>Menu</span>
        </v-btn>
        <v-list>
          <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
            <v-list-tile-title>{{ link.text }}</v-list-tile-title>
          </v-list-item>
        </v-list>
      </v-menu>
<!-- 
      <v-menu offset-y>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Dropdown
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
         
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu> -->

            <v-btn right flat color="grey">
                <span>Sign Out</span>
                <v-icon right large color="orange darken-2">mdi-arrow-up-bold-box-outline</v-icon>
            </v-btn>
        </v-toolbar>
        <v-navigation-drawer app v-model="drawer" class="success">
           <v-app-bar-nav-icon right @click="drawer=!drawer"></v-app-bar-nav-icon>
            <v-layout column align-center>
        <v-flex class="mt-5">
          <v-avatar size="100">
            <img class="text-lg-center" src="/image1.png">
          </v-avatar>
          <p class="white--text subheading mt-1">The Net Ninja</p>
        </v-flex>
        <v-flex class="mt-4 mb-3">
          <Popup/>
        </v-flex>
      </v-layout>
           <v-list>
             <v-list-item  v-for="link in links" :key="link.text" router :to="link.route">
                <v-list-item-action>
                   <v-icon>{{link.icon}}</v-icon>
                </v-list-item-action>
               <v-list-item-content>
                   <v-list-item-title>{{link.text}}</v-list-item-title>
               </v-list-item-content>
             </v-list-item>
           </v-list>
        </v-navigation-drawer>
    </nav>
</template>

<script>
import Popup from './Popup'
export default {
  components: { Popup },
     data(){
         return{
             drawer:false,
             links:[
                 {icon:'mdi-home',text:'Dashboard',route:'/'},
                 {icon:'mdi-home',text:'My Projects',route:'/projects'},
                 {icon:'mdi-home',text:'Team',route:'/team'}
             ]
         }
     }
}
</script>