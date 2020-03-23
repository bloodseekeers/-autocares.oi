<template>
  <v-app>
   <Nav/>
    <v-content>
      <Cabecera/>
      <HelloWord/>
    </v-content>
    <Piepage/>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Nav from './components/Nav';
import Piepage from './components/Piepage';
import Cabecera from './components/Cabecera';
export default {
  name: 'App',

  components: {
    HelloWorld, Nav, Piepage, Cabecera,
  },

  data: () => ({
    //
  }),
};
</script>
