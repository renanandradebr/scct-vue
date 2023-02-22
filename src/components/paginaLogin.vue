<template>
    <v-container class="fill-height">
      <v-row align="center" justify="center">
        <v-col md="4" sm="8">
          <v-card class="elevation-12">
            <v-toolbar color="primary" dark flat>
              <v-toolbar-title>Login</v-toolbar-title>
            </v-toolbar>
            <v-card-text>
              <v-form @submit.prevent="fazerLogin">
                <v-text-field v-model="email" label="E-mail"></v-text-field>
                <v-text-field v-model="senha" label="Senha" type="password"></v-text-field>
                <v-checkbox v-model="lembrarLogin" label="Lembrar Login"></v-checkbox>
                <v-btn type="submit" color="primary" block>Entrar</v-btn>
              </v-form>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    data() {
      return {
        email: '',
        senha: '',
        lembrarLogin: false
      }
    },
    methods: {
      fazerLogin() {
        // Aqui você pode fazer a lógica de autenticação do usuário
        console.log('Usuário autenticado!');
        
        // Define o valor da flag de lembrar login no localStorage
        if (this.lembrarLogin) {
          localStorage.setItem('lembrarLogin', true);
        } else {
          localStorage.removeItem('lembrarLogin');
        }
        
        // Redireciona o usuário para a página principal após o login
        this.$router.push('/');
      }
    },
    created() {
      // Carrega o valor da flag de lembrar login do localStorage
      if (localStorage.getItem('lembrarLogin') === 'true') {
        this.lembrarLogin = true;
      }
    }
  }
  </script>
  
  <style scoped>
  .toolbar {
    color: #fff;
  }
  </style>