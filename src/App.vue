<template>
  <v-app>
    <v-app-bar text max-height="65">
      <Header />
    </v-app-bar>

    <router-view></router-view>

    <!-- <v-content>
      <Carousel />
      <Buttons />
      <ContentInicialPage/>
    </v-content> -->
  </v-app>
</template>

<script>
import Header from "./components/Header";
// import Carousel from "./components/Carousel";
// import Buttons from "./components/Buttons";
// import ContentInicialPage from "./components/ContentInicialPage";
// import Footer from "./components/common/Footer";
export default {
  name: "App",
  components: {
    Header,
    // Carousel,
    // Buttons,
    // ContentInicialPage
    // Footer
  },
  data: () => ({
    //
  }),
};
</script>