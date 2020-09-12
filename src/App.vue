<template>
  <div class id="app">
    <div class="container grid-xs py-2">
      <img class="img-responsive img-logo" src="@/assets/photo.png" alt="Logo">
        <div>  
          <form @submit="addInfo">
            <!-- Vou Entrar com as minhas informações -->
            <div class="input-group entrada-info">
              <input type="text" v-model="info.description" class="form-input" id="name" placeholder="Name">  
              <input type="email" v-model="info.description" class="form-input" id="email" placeholder="E-mail">            
              <button class="btn input-group-btn">Add Informação</button>
              {{ info }}
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
      return {todos:[], info:{} };
    },
    // Methods informações dentro dos componentes    
    methods:{
      addInfo() {

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
  max-width: 350px;
  margin: 0 auto;
}

</style>