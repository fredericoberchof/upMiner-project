<template>
  <div class="team">
    <v-container>
      <v-btn class="teste" id="no-hover" text>
        <strong
          ><router-link class="deep-orange--text" to="/">
            <span><v-icon>arrow_back_ios</v-icon></span> Histórico
            Empresarial</router-link
          >
        </strong>
      </v-btn>
      <h1 class="subheading deep-orange--text"></h1>
    </v-container>

    <v-main class="my-5">
      <v-container>
        <v-carousel hide-delimiters cycle>
          <v-layout justify-center>
            <v-flex lg4>
              <v-carousel-item v-for="item in team" :key="item.name">
                <v-card class="s ma-1">
                  <v-responsive class="pt-4">
                    <img :src="item.icon" />
                  </v-responsive>
                  <v-card-text>
                    <div>
                      <strong class="darken-3--text text--lighten-1"
                        >{{ item.name }}
                      </strong>
                    </div>
                    <div class="deep-orange--text">{{ item.role }}</div>
                  </v-card-text>
                </v-card>
              </v-carousel-item>
            </v-flex>
          </v-layout>
        </v-carousel>
      </v-container>
      <v-container>
        <div class="grey--text text-justify">
          <h2>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod temporary incididunt ut labore et dolore magna aliqua. Enim
            adim ad minimim veniam, quis nostrud exercise ullamco laboris nisi
            ut alipip ex ea commodo consequat. Duis auteur irure pain in
            reprehenderit in voluptate velit this cillum dolore eu fugiat nulla
            pariatur. Excepteur sint occecat cupidatat non proident, sunt in
            culpa qui officia deserunt mollit anim id est laborum.
          </h2>
        </div>
        <div class="enablePrice row">
          <div class="price">
            <h1><strong>R$ 40,00</strong></h1>
          </div>
          <v-btn class="enableBtn white--text" depressed>
            <strong>Habilitar</strong>
          </v-btn>
        </div>
      </v-container>
    </v-main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      team: [
        {
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          icon: "/time-line.png",
        },
        {
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          icon: "/time-line.png",
        },
      ],
    };
  },
};
</script>

<style scoped>
.enableBtn {
  background: linear-gradient(to left, #f83600, #fe8c00);
}

.enablePrice {
  padding: 50px;
}

.price {
  margin-right: 30px;
}

.teste {
  font-size: 20px !important;
  margin-top: 30px;
}

.v-btn::before {
  background-color: transparent;
}
</style>

