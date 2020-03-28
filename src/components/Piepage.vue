<template>
  <v-card height="">
    <v-footer
        absolute
        color="green lighten-1"
        app
    >
      <v-col
        class="text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} —  <a href="mailto:titoderian48@gmail.com" class="white--text">D.Technology</a>
      </v-col>
    </v-footer>
  </v-card>
</template>
<style>
a{
  text-decoration: none;
  color: white;
}
</style>