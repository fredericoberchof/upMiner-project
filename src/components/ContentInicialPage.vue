<template>
  <div class="cards">
    <v-row align="center">
      <v-col class="order d-flex" cols="12" sm="3">
        <v-select
          @click="sortBy('name')"
          :items="classesName"
          v-model="foodType"
          label="Ordenar..."
          solo
        ></v-select>
      </v-col>
    </v-row>

    <v-main class="my-5" slot="items" scope="{ item }">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="product in cards" :key="product.name">
          <v-card class="text-center ma-3">
            <v-responsive class="pt-4">
              <v-avatar size="80">
                <img :src="product.icon" />
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div>
                <strong class="darken-3--text text--lighten-1"
                  >{{ product.name }}
                </strong>
              </div>
              <div class="grey--text">{{ product.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn
                @click.stop="openDialog = true"
                class="btnContent white--text"
                block
                text
              >
                <span class="price">{{ product.price }} </span>
                <strong>Saiba mais </strong>
              </v-btn>

              <v-row justify="center">
                <v-dialog
                  :retain-focus="false"
                  v-model="openDialog"
                  max-width="290"
                >
                  <v-card>
                    <v-card-title>
                      {{ product.name }}
                    </v-card-title>

                    <v-card-text>
                      {{ product.role }}
                    </v-card-text>

                    <v-card-actions>
                      <v-spacer></v-spacer>
                      <v-btn
                        color="red darken-1"
                        text
                        @click="openDialog = false"
                      >
                        Fechar
                      </v-btn>
                    </v-card-actions>
                  </v-card>
                </v-dialog>
              </v-row>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      openDialog: false,
      cards: [
        {
          name: "Profissional",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/images/professional.png",
        },
        {
          name: "Reguladores",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/images/temple.png",
        },
        {
          name: "Sócio Ambiental",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/images/tree.png",
        },
        {
          name: "Jurídico",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/images/gavel.png",
        },
        {
          name: "Listas restritivas",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/images/disable.png",
        },
        {
          name: "Mídia / Internet",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/images/midia.png",
        },
        {
          name: "Bens e imóveis",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/images/diamond.png",
        },
        {
          name: "Cadastro",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/images/person1.png",
        },
      ],
      classesName: ["Populares", "Lançamentos", "Nome", "A - Z"],
      foodType: null,
    };
  },
  methods: {
    sortBy(prop) {
      this.cards.sort((a, b) => (a[prop] < b[prop] ? -1 : 1));
    },
  },
};
</script>

<style>
.btnContent {
  background: linear-gradient(to left, #f83600, #fe8c00);
  justify-content: space-between;
}

.btnContent a {
  color: #fff !important;
}

.order {
  margin-top: 20px;
  margin-left: 5px;
}

.v-btn__content {
  display: flex !important;
}
</style>
