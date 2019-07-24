<template>
  <div>
    {{todos}}
    <todos v-model="todos"></todos>
    <todos v-model="todos"></todos>
    <button @click="addTodo"></button>
  </div>
</template>

<script>
import Todos from './components/Todos'

export default {
  data () {
    return {
      todos: [{
        name: 'Demo',
        completed: true
      }]
    }
  },
  components: {
    Todos
  },
  methods: {
    addTodo () {
      this.todos.push({
        name: 'Jean',
        completed: false
      })
    }
  }
}
</script>
<style src="./base.css"></style>
