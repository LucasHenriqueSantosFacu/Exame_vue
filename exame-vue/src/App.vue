<template>
  <div id="app">
    <Cadastro @item-adicionado="adicionarItem" />
    <Listagem :itens="itens" />
  </div>
</template>

<script>
import Cadastro from './components/Cadastro.vue';
import Listagem from './components/Listagem.vue';

export default {
  name: 'App',
  components: {
    Cadastro,
    Listagem
  },
  data() {
    return {
      itens: []
    };
  },
  methods: {
    adicionarItem(item) {
      this.itens.push(item);
    }
  }
};
</script>

<style>
/* Adicione seus estilos aqui */
</style>