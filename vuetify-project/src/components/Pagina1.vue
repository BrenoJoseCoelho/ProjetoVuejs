<style>
.card1 {
  background-color: blue !important;
}
</style>

<template>
  <v-container>
    <v-row>
      <v-col cols="4">
        <v-card class="card1">
          <v-card-text>
            <p>Coluna 1 - Pagina 1</p>
            <p>{{ texto1 }}</p>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card class="card1">
          <v-card-text>
            <p>Coluna 2 - Pagina 1 </p>
            <p>{{ texto2 }}</p>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card class="card1">
          <v-card-text>
            <p>Coluna 3 - Pagina 1</p>
            <p>{{ texto3 }}</p>
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
    texto3: {
        type: String,
        default: "Coluna 3"
    }
  }
};
</script>