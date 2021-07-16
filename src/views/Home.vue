<template>
  <v-main>
     <Carousel />
      <Buttons />
      <ContentInicialPage/>
  </v-main>
</template>

<script>
import Carousel from "@/components/Carousel";
import Buttons from "@/components/Buttons";
import ContentInicialPage from "@/components/ContentInicialPage";

export default {
  name: "Home",

  components: {
    Carousel,
    Buttons,
    ContentInicialPage,
  },
};
</script>
