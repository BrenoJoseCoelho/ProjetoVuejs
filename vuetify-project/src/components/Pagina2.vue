<style>
.card2 {
    background-color: chocolate !important;
}

</style>

<template>
  <v-container>
    <v-row>
      <v-col cols="6">
        <v-card class="card2">
          <v-card-text>
            <p class="text-h5">Coluna 1 - Pagina 2</p>
            <p class="text-subtitle-1">{{ texto1 }}</p>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="6">
        <v-card class="card2">
          <v-card-text>
            <p class="text-h5">Coluna 2 - Pagina 2</p>
            <p class="text-subtitle-1">{{texto2 }}</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">

export default {
   props: {
    texto1: {
        type: String,
        default: "Coluna 1"
    },
    texto2: {
        type: String,
        default: "Coluna 2"
    },
  }
};
</script>