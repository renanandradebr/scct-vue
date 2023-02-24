<template>
  <v-container class="d-flex justify-center align-center fill-height">
    <v-card class="pa-8" min-width="400">
      <h2 class="text-center mb-6">Solicitação de Backups</h2>
      <v-form v-model="valid">
        <v-text-field v-model="nome" label="Nome" required />
        <v-text-field v-model="email" label="E-mail" required :rules="emailRules" />
        <v-text-field v-model="pagina" label="Página" required />
        <v-text-field v-model="periodo" label="Período" required />
        <v-checkbox v-model="confirmacao" label="Confirmo que as informações fornecidas estão corretas" required />
        <v-btn v-if="valid" color="primary" class="mt-8" @click="enviarSolicitacao">
          Enviar Solicitação
        </v-btn>
      </v-form>
    </v-card>
  </v-container>
</template>
  
<script>
export default {
  data() {
    return {
      nome: "",
      email: "",
      pagina: "",
      periodo: "",
      confirmacao: false,
      valid: false,
      emailRules: [
        (v) => !!v || "E-mail é obrigatório",
        (v) => /.+@.+/.test(v) || "E-mail deve ser válido",
      ],
    };
  },
  methods: {
    enviarSolicitacao() {
      // Enviar a solicitação de backup para o servidor aqui
      console.log("Solicitação enviada!");
    },
  },
};
</script>
  
<style>

.fill-height {
  height: 100%;
}
</style>