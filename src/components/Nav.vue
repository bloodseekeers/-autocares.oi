<template>
    <div class="nav">
       <v-app-bar
         color = 'green lighten-1'
       >
       <!-- class="d-flex d-sm-none" -->
        <v-app-bar-nav-icon class="d-lg-none  d-xl-none"  @click.stop="drawer = !drawer"/>
        <v-toolbar-title class="white--text">Juan Parejo Autocares S.L</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn text class="d-none d-lg-flex  white--text"
         href="#servicios"
        >Servicios</v-btn>
        <v-btn text class="d-none d-lg-flex white--text"
         href="#empresa"
        >Empresa</v-btn>
        <v-btn text class="d-none d-lg-flex white--text"
         href="#contacto"
        >Contacto</v-btn>
       </v-app-bar>
        <v-navigation-drawer
         app
         v-model="drawer"
         absolute
         temporary
         color = 'green lighten-1'
       >
         <v-list>
            <v-list-item link href="#empresa">
               <v-list-item-action>
                  <v-icon>mdi-domain</v-icon>
               </v-list-item-action>
               <v-list-item-content>
                  <v-list-item-title class="white--text">Empresa</v-list-item-title>
               </v-list-item-content>
            </v-list-item>
            <v-list-item link href="#contacto" >
               <v-list-item-action>
                  <v-icon  >mdi-email</v-icon>
               </v-list-item-action>
               <v-list-item-content>
                  <v-list-item-title class="white--text">Contacto</v-list-item-title>
               </v-list-item-content>
            </v-list-item>
         </v-list>
       </v-navigation-drawer>
    </div>
</template>
<script>
export default {
   name: 'NavBar',
   data: () => ({
      drawer: null,

   })
}
</script>
<style>
a{
   text-decoration: none;
   color: white;
}
</style>