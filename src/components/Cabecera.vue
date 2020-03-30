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
            src: 'https://cdn.pixabay.com/photo/2019/08/19/12/31/london-4416306_960_720.jpg',
          },
          {
            src: 'https://cdn.pixabay.com/photo/2017/04/26/10/33/transport-2262256_960_720.jpg',
          },
          {
            src: 'https://cdn.pixabay.com/photo/2015/03/26/09/53/bus-690508_960_720.jpg',
          },
          {
            src: 'https://cdn.pixabay.com/photo/2015/11/21/15/21/london-bus-1055054_960_720.jpg',
          },
        ],
      }
    },
}
</script>
<style>
 @media screen (max-width: 1100px) {
   
 }
</style>