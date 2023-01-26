<template>
  <div>

    <h1 :class="{ 'title': true, 'title-home': isHome }">
      Curso Vue 3
    </h1>

    <p :class="['text']">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint debitis suscipit soluta! Esse doloremque voluptatem velit consequuntur consectetur, pariatur explicabo deleniti, excepturi sit, ex sed quasi possimus nam tenetur sint.
    </p>

    <p :style="{'color': 'aqua', 'background-color': 'black'}">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint debitis suscipit soluta! Esse doloremque voluptatem velit consequuntur consectetur, pariatur explicabo deleniti, excepturi sit, ex sed quasi possimus nam tenetur sint.
    </p>


    <div 
      v-for="objeto in todos"
      v-bind:key="objeto.id"
      class="todos-item"
    >

    <img 
      :src="objeto.imgSrc"
      >

      {{ objeto.title }}
    </div>


  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      classVar: 'title',
      isHome: true,
      pClass: 'text',
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false,
          "imgSrc": 'https://via.placeholder.com/150'

        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false,
          "imgSrc": 'https://via.placeholder.com/150'
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
.title{
  font-size: 20px;
}
.title-home{
  font-size: 40px;
  color: red;

}
.todos-item{
  background-color: black;
  color: #fff;
  margin: 0 0 5px 0;
  padding: 3px 6px;
}
.text{
  color: blue;
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
