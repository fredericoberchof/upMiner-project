<template>
  <v-col align="center">
    <v-btn class="btn"> <v-icon>language</v-icon> Todos </v-btn>
    <v-btn class="btn"><v-icon>work</v-icon> Profissional </v-btn>
    <v-btn class="btn"><v-icon>house_siding</v-icon> Reguladores </v-btn>
    <v-btn class="btn"><v-icon>park</v-icon> Sócio Ambiental </v-btn>
    <v-btn class="btn"><v-icon>gavel</v-icon> Jurídico </v-btn>
    <v-btn class="btn"><v-icon>unpublished</v-icon> Listas Restritivas</v-btn>
    <v-btn class="btn"><v-icon>public</v-icon> Mídia / Internet </v-btn>
    <v-btn class="btn"><v-icon>home_work</v-icon> Bens e Imóveis </v-btn>
    <v-btn class="btn"><v-icon>person</v-icon> Cadastro </v-btn>
    <v-btn class="btn"><v-icon>payments</v-icon> Fiananceiro </v-btn>
  </v-col>
</template>

<script>
export default {
  name: "Buttons",
  data: () => ({}),
};
</script>

<style scoped>
.btn {
  height: 80px !important;
  width: 120px !important;
}


.btn:hover {
  background: linear-gradient(to left, #f83600, #fe8c00) !important;
}

.v-icon {
  margin-bottom: 10px;
}
</style>