<template>
  <v-col align="center">
    <v-btn class="btnCards"> <v-icon>language</v-icon> Todos </v-btn>
    <v-btn class="btnCards"><v-icon>work</v-icon> Profissional </v-btn>
    <v-btn class="btnCards"><v-icon>house_siding</v-icon> Reguladores </v-btn>
    <v-btn class="btnCards"><v-icon>park</v-icon> Sócio Ambiental </v-btn>
    <v-btn class="btnCards"><v-icon>gavel</v-icon> Jurídico </v-btn>
    <v-btn class="btnCards"><v-icon>unpublished</v-icon> Listas Restritivas</v-btn>
    <v-btn class="btnCards"><v-icon>public</v-icon> Mídia / Internet </v-btn>
    <v-btn class="btnCards"><v-icon>home_work</v-icon> Bens e Imóveis </v-btn>
    <v-btn class="btnCards"><v-icon>person</v-icon> Cadastro </v-btn>
    <v-btn class="btnCards"><v-icon>payments</v-icon> Fiananceiro </v-btn>
  </v-col>
</template>

<script>
export default {
  name: "Buttons",
  data: () => ({}),
};
</script>

<style scoped>

.btnCards {
  height: 80px !important;
  width: 120px !important;
  margin-top: 20px !important;
}

.btnCards:hover {
  background: linear-gradient(to left, #f83600, #fe8c00) !important;
}

.v-btn.v-size--default {
  text-transform: capitalize !important;
  font-size: 0.720rem !important;
}

.v-icon {
  margin-bottom: 10px;
  position:absolute;
  margin-bottom: 50px;
}
</style>