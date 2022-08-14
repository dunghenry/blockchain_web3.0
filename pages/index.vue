<template>
  <div>
  <!-- {{getCounter}}
  <button v-on:click="increment">Increment</button> -->
  <!-- <TodoListVue/> -->
  <button v-on:click="getTodos">Get Todos</button>
  </div>
</template>

<script>
import TodoListVue from '../components/TodoList.vue';
import { mapGetters, mapMutations, mapActions} from 'vuex';
export default {
  name: 'IndexPage',
  components: {TodoListVue},
  computed: {...mapGetters(['getCounter'])},
  methods: {...mapMutations(['increment', 'GET_TODOS']), ...mapActions(['getTodos'])},
}
</script>
