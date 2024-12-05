<template>
  <div>
    <h2>Listagem</h2>
    <ul>
      <li v-for="(item, index) in itens" :key="index">
        <strong>{{ item.nome }}</strong>: {{ item.descricao }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    itens: {
      type: Array,
      required: true
    }
  }
};
</script>
