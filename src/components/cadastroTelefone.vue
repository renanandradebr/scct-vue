<template>
  <v-container fluid>
    <v-card>
      <v-card-title class="headline">Cadastro de Telefone Celular</v-card-title>
      <v-card-text>
        <v-form ref="form">
          <v-row>
            <v-col cols="12" md="6">
              <v-text-field v-model="nome" label="Nome" required></v-text-field>
            </v-col>
            <v-col cols="12" md="6">
              <v-text-field v-model="sobrenome" label="Sobrenome" required></v-text-field>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12" md="6">
              <v-text-field v-model="telefone" label="Telefone" required></v-text-field>
            </v-col>
            <v-col cols="12" md="6">
              <v-text-field v-model="operadora" label="Operadora"></v-text-field>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12" md="6">
              <v-text-field v-model="tipoPlano" label="Tipo de Plano"></v-text-field>
            </v-col>
            <v-col cols="12" md="6">
              <v-text-field v-model="valorPlano" label="Valor do Plano"></v-text-field>
            </v-col>
          </v-row>
        </v-form>
      </v-card-text>
      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn color="primary" @click="salvar">Salvar</v-btn>
        <v-btn color="error" to='./'  @click="cancelar">Cancelar</v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'CadastroTelefone',
  data() {
    return {
      nome: '',
      sobrenome: '',
      telefone: '',
      operadora: '',
      tipoPlano: '',
      valorPlano: '',
    };
  },
  methods: {
    salvar() {
      if (this.$refs.form.validate()) {
        // Lógica para salvar os dados
      }
    },
    cancelar() {
      // Lógica para cancelar o cadastro
    },
  },
});
</script>