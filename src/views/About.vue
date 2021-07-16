<template>
  <v-main>
    <Carousel />
    <Historic />
  </v-main>
</template>

<script>
import Historic from "@/components/Historic";
import Carousel from "@/components/Carousel";

export default {
  name: "About",
  components: {
    Historic,
    Carousel,
  },
};
</script>
