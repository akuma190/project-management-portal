<template>
    <nav>
        <v-toolbar flat app>
            <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="tex-uppercase grey--text">
            <span class="font-weight-light">Project</span>
            <span>Mangement</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn right flat color="grey">
                <span>Sign Out</span>
                <v-icon right large color="orange darken-2">mdi-arrow-up-bold-box-outline</v-icon>
            </v-btn>
        </v-toolbar>
        <v-navigation-drawer app v-model="drawer" class="success">
           <v-app-bar-nav-icon right @click="drawer=!drawer"></v-app-bar-nav-icon>
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
export default {
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