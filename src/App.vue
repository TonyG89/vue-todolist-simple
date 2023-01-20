<template>
  <div class="app">
    <TodoList :tasks="todos" @del-task="deleteTask"/>
  </div>
</template>

<script>
import TodoList from './components/TaskList.vue';

export default {
  name: 'App',
  data(){
    return{
      todos:['1','2','check']
    }
  },
  components: {
    TodoList
  },
  methods:{
    deleteTask(i){
      this.todos.splice(i, 1)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
