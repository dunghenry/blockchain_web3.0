<template>
  <div>
    <h1>TodoList Component</h1>
    <AddTodo/>
    <div v-for="todo in todos" :key="todo.id">
        <TodoItem :todo="todo" />
    </div>
    <TodoItem />
  </div>
</template>

<script>
import TodoItem from './TodoItem.vue';
import AddTodo from './AddTodo.vue';
export default {
  props: ['todos'],
  components: { TodoItem, AddTodo }
}
</script>

<style>

</style>