<template>
  <div class="cards">
    <!-- <v-layout row justify-start class="mb-3">
      <v-tooltip top>
        <v-btn color="grey" @click="sortBy('name')" slot="activator">
          <v-icon small left>folder</v-icon>
          <span class="caption text-lowercase">Ordenar</span>
        </v-btn>
        <span>Sort by project name</span>
      </v-tooltip>
    </v-layout> -->

    <v-row align="center">
      <v-col class="order d-flex" cols="12" sm="3">
        <v-select
          :items="classesName"
          v-model="foodType"
          label="Ordenar..."
          solo
        ></v-select>
      </v-col>
    </v-row>

    <v-main class="my-5" slot="items" scope="{ item }">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="person in cards" :key="person.name">
          <v-card class="text-center ma-3">
            <v-responsive class="pt-4">
              <v-avatar size="80">
                <img :src="person.icon" />
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div>
                <strong class="darken-3--text text--lighten-1"
                  >{{ person.name }}
                </strong>
              </div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn class="btnContent white--text" block text>
                <span class="price">{{ person.price }} </span>
                <strong
                  ><router-link to="/about">Saiba mais</router-link>
                </strong>
              </v-btn>
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
      cards: [
        {
          name: "Profissional",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/professional.png",
        },
        {
          name: "Reguladores",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/temple.png",
        },
        {
          name: "Sócio Ambiental",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/tree.png",
        },
        {
          name: "Jurídico",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/gavel.png",
        },
        {
          name: "Listas restritivas",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/disable.png",
        },
        {
          name: "Mídia / Internet",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/midia.png",
        },
        {
          name: "Bens e imóveis",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/diamond.png",
        },
        {
          name: "Cadastro",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam...",
          price: "R$ 29,99",
          icon: "/person1.png",
        },
      ],
      classesName: [
        "Profissional",
        "Reguladores",
        "Sócio Ambiental",
        "Jurídico",
        "Listas restritivas",
        "Mídia / Internet",
        "Bens e imóveis",
        "Cadastro",
      ],
      foodType: null,
    };
  },

  computed: {
    filteredItems() {
      return this.cards.filter((i) => {
        console.log(this.cards);
        return !this.foodType || i.type === this.foodType;
      });
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
