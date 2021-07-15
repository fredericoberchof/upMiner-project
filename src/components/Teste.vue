<template>
  <div class="team">
    <h1 class="subheading grey--text">Team</h1>

    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
          <v-card class="text-center ma-3">
            <v-responsive class="pt-4">
              <v-avatar size="80" >
                <img :src="person.icon" />
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn block flat>
                <span class="">{{ person.price }} </span>
                <span class="">Saiba mais </span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      team: [
        {
          name: "Profissional",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis",
          price: "R$ 29,99",
          icon: "/professional.png",
        },
        {
          name: "Reguladores",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis",
          price: "R$ 29,99",
          icon: "/temple.png",
        },
        {
          name: "Sócio Ambiental",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis",
          price: "R$ 29,99",
          icon: "/tree.png"
        },
        {
          name: "Jurídico",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis",
          price: "R$ 29,99",
          icon: "/gavel.png"
        },
        {
          name: "Listas restritivas",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis",
          price: "R$ 29,99",
          icon: "/disable.png"
        },
        {
          name: "Mídia / Internet",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis",
          price: "R$ 29,99",
          icon: "/midia.png"
        },
        {
          name: "Bens e imóveis",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis",
          price: "R$ 29,99",
          icon: "/diamond.png"
        },
        {
          name: "Cadastro",
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis",
          price: "R$ 29,99",
          icon: "/person1.png"
        },
      ],
    };
  },
};
</script>

<style  scoped>
</style>>

