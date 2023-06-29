<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" app>
      <v-list>
    <v-list-item class="text-h5"><button @click="changeComponent(1)"> Pagina 1</button></v-list-item>
    <v-list-item class="text-h5"><button @click="changeComponent(2)"> Pagina 2</button></v-list-item>


      </v-list>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
         <v-toolbar-title class="text-h4">Meu App</v-toolbar-title>
    </v-app-bar>

    <v-main>
        <component :is="currentComponent" :texto1="prop1" :texto2="prop2" :texto3="prop3"></component>
    </v-main>
  </v-app>
  
</template>

<script lang="ts">
import ComponentePagina1 from '../components/Pagina1.vue';
import ComponentePagina2 from '../components/Pagina2.vue';

const variavel1: String = "Valor da Variavel 1 para a Página 1";
const variavel2: String = "Valor da Variavel 2 para a Página 1";
const variavel3: String = "Valor da Variavel 3 para a Página 1";
const variavel4: String = "Valor da Variavel 1 para a Página 2";
const variavel5: String = "Valor da Variavel 2 para a Página 2";

export default {
  components: {
    ComponentePagina1,
    ComponentePagina2
  },
  data() {
    return {
      drawer: false,
      currentComponent: ComponentePagina1,
      prop1: 'coluna 1',
      prop2: 'coluna 2',
      prop3: 'coluna 3'
    };
  },
  methods: {
    changeComponent(page) {
      if (page === 1) {
        this.currentComponent = ComponentePagina1;
        this.prop1 = variavel1;
        this.prop2 = variavel2;
         this.prop3 = variavel3;
      } else if (page === 2) {
        this.currentComponent = ComponentePagina2;
        this.prop1 = variavel4;
        this.prop2 = variavel5;
      }
    }
  }
};

</script>