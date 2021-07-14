<template>
  <v-app>
    <v-app-bar flat max-height="65">
      <Header />
    </v-app-bar>

    <v-content>
      <Carousel />
    </v-content>
  </v-app>
</template>

<script>
import Header from "./components/Header";
import Carousel from "./components/Carousel";
// import Footer from "./components/common/Footer";
export default {
  name: "App",
  components: {
    Header,
    Carousel,
    // Footer
  },
  data: () => ({
    //
  }),
};
</script>