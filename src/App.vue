<template>
  <div>

   {{ user.first_name }} {{ user.last_name }}

  </div> 
  <br>
  <div>

   {{ fullName }}

  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      user: {
        first_name:'Ana',
        last_name:'Bull'
      }
    }
  },
  computed: {
    fullName(){
      return `${this.user.first_name} ${this.user.last_name}`
    }
    // Computed é usado quando voce só quer computar o valor uma vez, não ocupando tanta memória
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
