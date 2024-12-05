<template>
  <div>
    <h2>Cadastro</h2>
    <form @submit.prevent="adicionarItem">
      <div>
        <label for="nome">Nome:</label>
        <input type="text" v-model="nome" id="nome" required />
      </div>
      <div>
        <label for="descricao">Descrição:</label>
        <input type="text" v-model="descricao" id="descricao" required />
      </div>
      <button type="submit">Adicionar</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nome: '',
      descricao: ''
    };
  },
  methods: {
    adicionarItem() {
      this.$emit('item-adicionado', { nome: this.nome, descricao: this.descricao });
      this.nome = '';
      this.descricao = '';
    }
  }
};
</script>

