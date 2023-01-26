<template>
  <div>

    <div>
      One-way data binding <br>
      <!-- É quando somente o sistema consegue alterar informações.  -->
      Two-way data binding (bidirecional)<br>
      <!-- Quando o sistema e o usuários conseguem atualizar um valor, um formulário, por exemplo. Utiliza-se o v-model -->
      v-model -> formulários
    </div>

    <div>
      <input v-model="name" type="text">
      <!-- O v-model pega o que o usuário digitou no input e consegue colocar na variável -->
      <br>
      {{ name }}
    </div>

    <br>

    <div>
      <label>Sports</label>
      <br>
      <select v-model="sports">
        <option value="">Escolha</option>
        <option value="futebol">Futebol</option>
        <option value="skate">Skate</option>
        <option value="volei">Volei</option>
      </select>
      <br>
      {{ sports }}
    </div>
    <br>

    <div>
      <label>Newsletter</label>
      <br>
      <input type="radio" value="Sim" v-model="newsletter"> Sim
      <input type="radio" value="Não" v-model="newsletter"> Não
      <br>
      {{ newsletter }}

    </div>
    <br>

    <div>
      <label>Contrato</label>
      <br>
      <input type="checkbox" v-model="contrato"> Aceita nosso termos...
      <br>
      {{ contrato }}

    </div>
    <br>

    <div>
      <label>Cores que você mais gosta</label>
      <br>
      <input type="checkbox" value="Azul" v-model="colors"> Azul
      <input type="checkbox" value="Amarelo" v-model="colors"> Amarelo
      <br>
      {{ colors }}

    </div>

  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: 'Ana',
      sports: '',
      newsletter: '',
      contrato: '',
      colors: [],
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
