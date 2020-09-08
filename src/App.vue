<template>
  <div id="principal">
    <h1>SORTEIO do BRONX</h1>
    <div>
      <div class="name">
          <input type="text" name="nome" placeholder="Informe seu nome" required="required" autofocus>
      </div>
      <div class="email">
          <input type="email" name="email" placeholder="Informe seu e-mail" required="required">
      </div>
      <button @click="addinfo()">Add Dado</button>
    </div>
    <button @click="sortear()">Click para Sortear</button>
  </div>
</template>

<script>
  export default {
    nome: 'app'
  }
</script>

<style>

#principal{
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #2c3e50;
  border: 5px solid silver;
  color: blue;
  margin: 100px;
}

</style>