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
            <p>Coluna 1 - Pagina 2</p>
            <p>{{ texto1 }}</p>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="6">
        <v-card class="card2">
          <v-card-text>
            <p>Coluna 2 - Pagina 2</p>
            <p>{{texto2 }}</p>
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