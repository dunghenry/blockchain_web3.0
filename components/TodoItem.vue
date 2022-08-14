<template>
  <div>
    <h1>TodoItem Component</h1>
    <div>
      <h3>{{todo?.id}}</h3>
      <h3>{{todo?.title}}</h3>
      <p>{{todo?.completed}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoItem',
  props: ['todo']
}
</script>

<style>

</style>