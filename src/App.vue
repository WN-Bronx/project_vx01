<template>
  <div class id="app">
    <div class="container grid-xs py-2">
      <img class="img-responsive img-logo" src="@/assets/photo.png" alt="Logo">
        <div>  
          <form>
            <!-- Vou Entrar com as minhas informações -->
            <div class="input-group entrada-info">
              <input type="text" v-model="todo.description" class="form-input" id="name" placeholder="Name">  
              <input type="email" v-model="todo.description" class="form-input" id="email" placeholder="E-mail">            
              <button class="btn input-group-btn">Add Informação</button>
              {{ todo }}
            </div>
          </form>
        </div>  
    </div>  
  </div>  
</template>

<script>
  export default {
    nome: 'app',
    // Data será o estado do meu componente, vai retornar meus dados    
    data(){
      return {todos:[], todo:{} };
    },
    // Methods informações dentro dos componentes    
    methods:{
      addTodo() {}
    }
  }
</script>

<!-- Scoped so serve para a clase atual-->
<style scoped>
.img-logo{
  max-width: 100px;
  margin: 0 auto;
}

.entrada-info{
  max-width: 350px;
  margin: 0 auto;
}

</style>