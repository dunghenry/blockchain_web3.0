<template>
  <div>
    <TodoListVue :todos="todos" />
  </div>
</template>

<script>
import TodoListVue from '../components/TodoList.vue';
import { mapGetters, mapActions, mapMutations, mapState} from 'vuex';
export default {
  name: 'IndexPage',
  components: {TodoListVue},
  created(){
    this.setTodos()
  },
  // computed:{
  //   todos(){
  //     return this.$store.state.todos
  //   }
  // },
  computed: {...mapGetters("todos", ['getTodos']), ...mapState("todos", ["todos"])},
  methods: {...mapMutations("todos", []), ...mapActions("todos", ['setTodos'])},
}
</script>
