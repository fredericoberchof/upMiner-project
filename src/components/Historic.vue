<template>
  <div class="team">
    <h1 class="subheading deep-orange--text">Histórico Empresarial</h1>

    <v-main class="my-5">
      <v-container>
        <v-carousel hide-delimiters >
          <v-layout row justify-center>
            <v-flex lg4 v-for="person in team" :key="person.name">
              <v-carousel-item>
                <v-card class="text-justify ma-1">
                  <v-responsive class="pt-4">
                    <img :src="person.icon" />
                  </v-responsive>
                  <v-card-text>
                    <div>
                      <strong class="darken-3--text text--lighten-1"
                        >{{ person.name }}
                      </strong>
                    </div>
                    <div class="deep-orange--text">{{ person.role }}</div>
                  </v-card-text>
                  <v-card-actions> </v-card-actions>
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
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis",
          icon: "/time-line.png",
        },
        {
          role: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis",
          icon: "/time-line.png",
        },
        
      ],
    };
  },
};
</script>

