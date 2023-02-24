<template>
  <v-container>
    <div>
      
    </div>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img :src="require('../assets/logo-scct.png')" class="my-4 " contain height="120" />
      </v-col>

    </v-row>


    <v-divider class="my-3"></v-divider>
    <v-row>

      <v-col cols="4" class="pa-4 my-4">
        <v-container>
          <v-row  justify="center" >
            <div class="botoes">
            <v-btn block color="primary" class="mb-2" to='./cadastro' elevation="1" outlined> 
              <v-icon>mdi-account-plus</v-icon> CADASTRO DE USUÁRIO</v-btn>

            <v-btn block color="primary" class="mb-2" to='./cadastroTelefone' elevation="1" outlined>  <v-icon>mdi-phone-plus</v-icon>CADASTRO DE TELEFONE FIXO</v-btn>

            <v-btn block color="primary" class="mb-2" elevation="1" outlined> <v-icon>mdi-plus</v-icon>CADASTRO DE TELEFONE
              CELULAR</v-btn>

            <v-btn block color="primary" class="mb-2" elevation="1" outlined> <v-icon>mdi-deskphone</v-icon>AGENDA TELEFÔNICA</v-btn>

            <v-btn block color="primary" class="mb-2" to='./backups'  elevation="1" outlined> <v-icon>mdi-cloud-upload</v-icon>SOLICITAR BACKUPS</v-btn>

            <v-btn block color="primary" class="mb-2" elevation="1" outlined> <v-icon>mdi-phone-log</v-icon>ACESSAR LOGS DE USUÁRIO</v-btn>
          </div>
          </v-row>
        </v-container>
      </v-col>

      <v-col cols="8">
        <div class="carousel-container">
          <v-carousel hide-delimiters cycle height="400" style="max-width: 600px; margin: 0 auto;">
            <v-carousel-item v-for="item in items" :key="item.title" :src="item.image">
           
            </v-carousel-item>
          </v-carousel>
        </div>
      </v-col>


    </v-row>
    <v-divider></v-divider>

    <v-row>
      <v-col>

      </v-col>
    </v-row>
  </v-container>
</template>



<script>
export default {
  data() {
    return {
      items: [
        {
         
        },
        {
          image: "https://images.unsplash.com/photo-1488509082528-cefbba5ad692?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80",
        },
        {
          image: "https://images.unsplash.com/photo-1512428559087-560fa5ceab42?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80",
        },
      ],
    };
  },
};
</script>
<style>
.carousel-container {
  margin: 24px;
  margin-left: 2px;
}
.botoes{
  margin-left: 25px;
align-content: center;
}

</style>