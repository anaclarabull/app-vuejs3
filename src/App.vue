<template>
  <div>


    <div 
      v-for="objeto in todos"
      v-bind:key="objeto.id"
      class="todos-item"
    >
      <!-- <div v-for="objeto in array">: "objeto" é um objeto e o "todos" é um array -->
      {{ objeto.title }}
      <!-- objeto acessando uma propriedade dentro do objeto, o qual está apontando para os arrays -->
    </div>


  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
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
  }
}
</script>

<style>
.todos-item{
  background-color: black;
  color: #fff;
  margin: 0 0 5px 0;
  padding: 3px 6px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
