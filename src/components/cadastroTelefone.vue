<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" sm="8" md="6">
        <v-card>
          <v-card-title class="headline text-center">Cadastro de Usuário</v-card-title>
          <v-card-text>
            <v-form @submit.prevent="submit">
              <v-text-field v-model="form.name" label="Nome" required></v-text-field>
              <v-text-field v-model="form.email" label="E-mail" type="email" required></v-text-field>
              <v-text-field v-model="form.password" label="Senha" type="password" required></v-text-field>
              <v-text-field v-model="form.confirmPassword" label="Confirme a senha" type="password" required></v-text-field>
              <v-text-field v-model="form.setor" label="Setor"></v-text-field>
              <v-text-field v-model="form.matricula" label="Matrícula"></v-text-field>
              <v-btn type="submit" color="primary">Cadastrar</v-btn>
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
      form: {
        name: '',
        email: '',
        password: '',
        confirmPassword: '',
        setor: '',
        matricula: ''
      }
    }
  },
  methods: {
    submit() {
      // Lógica para submeter o formulário
    }
  }
}
</script>