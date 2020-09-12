<template>
  <div class id="app">
    <div class="container grid-xs py-2">
      <img class="img-responsive img-logo" src="@/assets/photo.png" alt="Logo">
        <div>  
          <form @submit.prevent="addInfo(info)">
            <!-- Vou Entrar com as minhas informações -->
            <div class="input-group">
              <input type="text" v-model="info.description" class="form-input" id="name" placeholder="Name">  
              <!--input type="email" v-model="info.description" class="form-input" id="email" placeholder="Email"-->            
              <button class="btn input-group-btn">Add Informação</button>
            </div>
            <!-- {{ todos }} -->
          </form>
          <!-- Mostra as minhas informações adicionadas -->
          <div class="info-list">
            <addPessoa v-for="i in todos" :key="i.id" :info="i" />
          </div>
        </div>  
    </div>  
  </div>  
</template>

<script>
  // Importando os Components
  import AddPessoa from "./components/AddPessoa";

  export default {
    nome: 'app',
    components: { AddPessoa },
    // Data será o estado do meu componente, vai retornar meus dados    
    data(){
      return {todos:[], info:{ checked: false} };
    },
    // Methods informações dentro dos componentes    
    methods:{
      addInfo(info) {
          info.id = Date.now();
          this.todos.push(info);
          this.info = { checked: false};
      }
    }
  }
</script>

<!-- Scoped so serve para a clase atual-->
<style scoped>
.img-logo{
  max-width: 120px;
  margin: 0 auto;
}

.entrada-info{
  max-width: 450px;
  margin: 0 auto;
}

.info-list{
  margin-top: 5px;
  padding-top: 2rem;
}

</style>