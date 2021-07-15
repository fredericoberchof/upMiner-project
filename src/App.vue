<template>
  <v-app>
    <v-app-bar flat max-height="65">
      <Header />
    </v-app-bar>

    <v-content>
      <Carousel />
      <Buttons />
      <Teste/>
    </v-content>
  </v-app>
</template>

<script>
import Header from "./components/Header";
import Carousel from "./components/Carousel";
import Buttons from "./components/Buttons";
import Teste from "./components/Teste";
// import Footer from "./components/common/Footer";
export default {
  name: "App",
  components: {
    Header,
    Carousel,
    Buttons,
    Teste
    // Footer
  },
  data: () => ({
    //
  }),
};
</script>