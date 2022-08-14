<template>
  <div>
    <h1>Todo Detail Page</h1>
   <div>
      <h3>{{todo?.id}}</h3>
      <h3>{{todo?.title}}</h3>
      <p>{{todo?.completed}}</p>
    </div>
  </div>
</template>

<script>
import { mapActions, mapState } from 'vuex';
export default {
  created(){
    this.getTodoById(this.$route.params.id)
  },
  computed: { ...mapState("todos", ["todos", "todo"]) },
  methods: {  ...mapActions("todos", ["setTodos", "getTodoById"]) }
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
}
</style>