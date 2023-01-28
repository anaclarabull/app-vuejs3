<template>
  <div>

    {{ user.first_name }} {{ user.last_name }}

  </div>
  <br>

  <div>

    {{ fullName }}

    <h2>To dos em aberto</h2>

    <div v-for="todo in uncompletedTodos" :key="todo.id">
      {{ todo.title }}
      <span>{{ todo.completed }}</span>
    </div>

    <h2>To dos completas</h2>

    <div v-for="todo in completedTodos" :key="todo.id">
      <!-- v-for: Vou pegar algo (nome qualquer -todo-) dentro de "todos" -->
      {{ todo.title }}
      <span>{{ todo.completed }}</span>
    </div>

    <h2>All To dos</h2>

    <div v-for="todo in todos" :key="todo.id">
      <input type="checkbox" v-model="todo.completed" >
      {{ todo.title }}
    </div>


  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      user: {
        first_name: 'Ana',
        last_name: 'Bull'
      },
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false
        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
        }
      ]
    }
  },

  computed: {
    fullName() {
      return `${this.user.first_name} ${this.user.last_name}`
    },
    // Computed é usado quando voce só quer computar o valor uma vez, não ocupando tanta memória

    uncompletedTodos() {
      return this.todos.filter(todo => !todo.completed);
      // Aqui foi feito um filtro para retornar as "to do" que não tem o completed (ou seja, que o comleted ta "false"). Caso queira as completadas, é só tirar o símbolo de negação "!".
    },
    completedTodos() {
      return this.todos.filter(todo => todo.completed);
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
