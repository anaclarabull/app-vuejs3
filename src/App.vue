<template>
  <TheHeader v-if="showHeader"/>
  <div v-show="showName">
    Nome: {{ firstName }} <br>
    Sobrenome: {{ lastName }}
  </div>

  <div v-if="acessLevel === 'admin'">Admin</div>
  <div v-else-if="acessLevel === 'mkt'">Marketing</div>
  <div v-else>User</div>

  <img alt="Vue logo" src="./assets/logo.png">

  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue';

// objeto que contém os atributos/variáveis do componente
export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader,
  },
  data() {
    // objeto reativo, onde as variáveis retivas estarão
    return {
      showHeader: true,
      firstName: 'Ana',
      lastName: 'Bull',
      showName: false,
      acessLevel: 'user',
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
