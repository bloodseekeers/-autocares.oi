<template>
    <div class="nav">
       <v-navigation-drawer class="d-flex d-sm-none"
         app
         v-model="drawer"
         clipped
         color = 'green lighten-1'
         disable-route-watcher
       >
         <v-list>
            <v-list-item link>
               <v-list-item-action>
                  <v-icon>mdi-domain</v-icon>
               </v-list-item-action>
               <v-list-item-content>
                  <v-list-item-title class="white--text">Sobre Nosotros</v-list-item-title>
               </v-list-item-content>
            </v-list-item>
            <v-list-item link>
               <v-list-item-action>
                  <v-icon>mdi-email</v-icon>
               </v-list-item-action>
               <v-list-item-content>
                  <v-list-item-title class="white--text">Contacto</v-list-item-title>
               </v-list-item-content>
            </v-list-item>
         </v-list>
       </v-navigation-drawer>
       <v-app-bar
         app
         clipped-left
         color = 'green lighten-1'
       >
        <v-app-bar-nav-icon class="d-flex d-sm-none" @click.stop="drawer = !drawer"/>
        <v-toolbar-title class="white--text">Juan Parejo Autocares S.L</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn text class="d-none d-sm-flex white--text">Servicios</v-btn>
        <v-btn text class="d-none d-sm-flex white--text">Empresa</v-btn>
        <v-btn text class="d-none d-sm-flex white--text">Contacto</v-btn>
       </v-app-bar>
    </div>
</template>
<script>
export default {
   name: 'NavBar',
   data: () => ({
      drawer: false,

   })
}
</script>
<style>

</style>