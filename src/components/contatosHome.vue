<template>
    <v-container fluid>
      <v-card>
        <v-card-title>
          Contatos
        </v-card-title>
        <v-card-text>
          <v-list>
            <v-list-item v-for="(contato, index) in contatos" :key="index">
              <v-list-item-avatar>
                <v-icon>mdi-account-circle</v-icon>
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>{{ contato.nome }}</v-list-item-title>
                <v-list-item-subtitle>{{ contato.email }}</v-list-item-subtitle>
                <v-list-item-subtitle>{{ contato.telefone }}</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card-text>
      </v-card>
    </v-container>
  </template>
  
  <script>
  export default {
    data() {
      return {
        contatos: [
          {
            nome: 'João Silva',
            email: 'joao.silva@example.com',
            telefone: '(11) 1234-5678'
          },
          {
            nome: 'Maria Souza',
            email: 'maria.souza@example.com',
            telefone: '(21) 9876-5432'
          },
          {
            nome: 'José Santos',
            email: 'jose.santos@example.com',
            telefone: '(31) 4567-8901'
          }
        ]
      };
    }
  };
  </script>