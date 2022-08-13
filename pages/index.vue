<template>
  <div>
  {{getCounter}}
  <button v-on:click="increment">Increment</button>
  </div>
</template>

<script>
import { mapGetters, mapMutations} from 'vuex'
export default {
  name: 'IndexPage',
  computed: {...mapGetters(['getCounter'])},
  methods: {...mapMutations(['increment'])}
}
</script>
