<template>
  <div>

    <button v-on:click="onClick">
      <!-- Capture quando tiver um evento do elemento, nesse caso o evento é o click -->
      Enviar
    </button>

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
