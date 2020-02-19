<template>
  <div class="hello">
    <div style="display:flex" v-for="(tarefa) in tarefas" v-bind:key="tarefa">
      <p>A tarefa {{tarefa.descricao}} está:</p>
      <p v-if="tarefa.estaCompleta == true" style="color:blue;marginStart:5px">Completa</p>
      <p v-else style="color:red">Incompleta</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {},
  data() {
    return {
      tarefas: [
        { id: 1, descricao: "Jim Carey", estaCompleta: true },
        { id: 2, descricao: "Beber", estaCompleta: true },
        { id: 3, descricao: "Matar", estaCompleta: false },
        { id: 4, descricao: "Beringela", estaCompleta: true }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
