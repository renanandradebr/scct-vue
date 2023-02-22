<template>
  <v-container fluid>
    <v-form v-model="valid">
      <h2>Cadastro de Usuário</h2>
      <v-divider></v-divider>
      <v-text-field v-model="nome" label="Nome completo" required></v-text-field>
      <v-text-field v-model="email" label="E-mail" type="email" required></v-text-field>
      <v-text-field v-model="senha" label="Senha" type="password" required></v-text-field>
      <v-text-field v-model="confirmSenha" label="Confirme a senha" type="password" required></v-text-field>
      <v-select v-model="sexo" :items="sexos" label="Sexo" required></v-select>
      <v-select v-model="setor" :items="setores" label="Setor" required></v-select>
      <v-text-field v-model="matricula" label="Matrícula" required></v-text-field>
      <v-checkbox v-model="aceitaTermos" label="Aceito os termos e condições" required></v-checkbox>
      <v-btn color="primary" dark :disabled="!valid" @click="cadastrar">Cadastrar</v-btn>
    </v-form>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      nome: '',
      email: '',
      senha: '',
      confirmSenha: '',
      sexo: null,
      setor: null,
      matricula: '',
      aceitaTermos: false,
      valid: false,
      sexos: ['Masculino', 'Feminino', 'Outro'],
      setores: ['RH', 'TI', 'Financeiro', 'Comercial', 'Operacional']
    }
  },
  methods: {
    cadastrar() {
      // Aqui você pode implementar a lógica para enviar os dados do formulário para o servidor
      // ou para o armazenamento local.
      console.log('Dados do formulário:', {
        nome: this.nome,
        email: this.email,
        senha: this.senha,
        sexo: this.sexo,
        setor: this.setor,
        matricula: this.matricula,
        aceitaTermos: this.aceitaTermos
      });
    }
  }
}
</script>