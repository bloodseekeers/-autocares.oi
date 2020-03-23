<template>
 <v-row
    fluid
    mt-1
  >
     <v-img
        :src="require('../assets/autocar1.jpeg')"
        height="325"
        class="grey darken-4"
     ></v-img>
    </v-row>
</template>
<script>
export default {
    name: 'Cabecera',
     data: () => ({
      show: false,
    }),
}
</script>
<style>

</style>