<template>
  <v-carousel hide-delimiters>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
</template>
<script>
export default {
     data () {
      return {
        items: [
          {
            src: 'img/autocar1.jpeg',
          },
          {
            src: 'img/header1.jpg',
          },
        ],
      }
    },
}
</script>
<style>

</style>