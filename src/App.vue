<template>
  <v-app>
   <Nav/>
    <v-content>
      <section id="cabecera">
        <Cabecera/>
      </section>
      <section id="servicios">
        <Servicios/>
      </section>
      <section>
        <Empresa/>
      </section>
      <section id="contacto">
        <Contacto/>
      </section>
    </v-content>
    <Piepage/>
  </v-app>
</template>

<script>
import Nav from './components/Nav';
import Piepage from './components/Piepage';
import Cabecera from './components/Cabecera';
import Servicios from './components/Servicios';
import Empresa from './components/Empresa';
import Contacto from './components/Contacto';
export default {
  name: 'App',

  components: {
  Nav, Piepage, Cabecera,Servicios,Empresa,Contacto,
  },

  data: () => ({
    //
  }),
};
</script>
<style>
  #app{
    background-color:rgb(245, 245, 245) ;
  }
</style>