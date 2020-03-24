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
    </v-content>
    <Piepage/>
  </v-app>
</template>

<script>
import Nav from './components/Nav';
import Piepage from './components/Piepage';
import Cabecera from './components/Cabecera';
import Servicios from './components/Servicios';
export default {
  name: 'App',

  components: {
  Nav, Piepage, Cabecera,Servicios,
  },

  data: () => ({
    //
  }),
};
</script>
