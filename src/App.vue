<template>
  <div>

    <button v-on:click="onClick">
      <!-- Capture quando tiver um evento do elemento, nesse caso o evento é o click -->
      <!-- v-on pode ser substituido por @. ex: @click -->
      Enviar
    </button>
    <br>

    <button v-on:click.once="onClickOnce">
      <!-- Só vai disparar o evento uma vez por causa do "once". Esses são chamados de Modificadores de Eventos -->
      Enviar
    </button>

    <div @mouseover="onMouseOver">
      Mouse Over
    </div>
    <br>

    <form action="https://www.google.com.br/" @submit="onSubmit">
      <button type="submit">
        <!-- type="submit" utiizado para enviar informações -->
      Enviar
    </button>
    </form>

  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
    }
  },

  methods:{
    onClick(){
      console.log('click')
    },
    onClickOnce(){
      console.log('click')
    },
    onMouseOver(){
      console.log('mouse over')
    },
    onSubmit(){
      console.log('submit')
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
