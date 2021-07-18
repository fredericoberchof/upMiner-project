<template>
  <v-toolbar text class="mainHeader">
    <img class="mr-3" :src="require('@/assets/upminer.png')" />
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-xs-only">
      <v-btn text><router-link to="/">Home</router-link></v-btn>
      <v-btn text><router-link to="/about">Saiba mais</router-link></v-btn>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {
  name: "Header",
  data() {},
};
</script>

<style>
.v-toolbar__content,
.v-toolbar__extension {
  padding: 1px !important;
}
</style>
