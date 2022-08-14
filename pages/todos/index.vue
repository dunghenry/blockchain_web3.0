<template>
  <div>
     <h1>Todos Page</h1>
     <TodoList :todos="todos"/>
  </div>
</template>

<script>
import { mapActions, mapState } from 'vuex';
import TodoList from '../../components/TodoList.vue';
export default {
  created() {
    this.setTodos();
  },
  computed: {...mapState("todos", ["todos"])},
  methods: { ...mapActions("todos", ["setTodos"]) },
  components: { TodoList }
}
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
}
</style>