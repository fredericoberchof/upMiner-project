<template>
  <div class="carouselBlock">
    <v-carousel hide-delimiters vertical-delimiters cycle>
      <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src">
        <v-row class="fill-height title" align="center" justify="center">
          <div>{{ item.title }}</div>
        </v-row>
      </v-carousel-item>
    </v-carousel>
    <div class="divider">
      <v-divider></v-divider>
    </div>
  </div>
</template>

<script>
export default {
  name: "Carrosel",
  data() {
    return {
      items: [
        {
          src: "./images/bannermain.jpeg",
          title: "upMiner",
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
          title: "Céu com nuvens",
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
          title: "Águia linda",
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg",
          title: "Planeta estranho",
        },
      ],
    };
  },
};
</script>

<style>
.divider {
  background: linear-gradient(to left, #f83600, #fe8c00);
  height: 5px;
}
</style>
