<template>
  <v-container class="fill-height" fluid>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="8" md="6">
        <v-card>
          <v-card-title class="text-center">Cadastro de Usuário</v-card-title>
          <v-card-text>
            <v-form @submit.prevent="submit">
              <v-text-field
                v-model="nome"
                label="Nome Completo"
                required
              ></v-text-field>
              <v-text-field
                v-model="email"
                label="E-mail"
                type="email"
                required
              ></v-text-field>
              <v-select
                v-model="sexo"
                :items="['Masculino', 'Feminino', 'Outro']"
                label="Sexo"
                required
              ></v-select>
              <v-text-field
                v-model="nascimento"
                label="Data de Nascimento"
                type="date"
                required
              ></v-text-field>
              <v-text-field
                v-model="cpf"
                label="CPF"
                required
              ></v-text-field>
              <v-text-field
                v-model="telefone"
                label="Telefone"
                required
              ></v-text-field>
              <v-text-field
                v-model="setor"
                label="Setor"
                required
              ></v-text-field>
              <v-text-field
                v-model="matricula"
                label="Matrícula"
                required
              ></v-text-field>
              <v-checkbox
                v-model="termos"
                label="Li e concordo com os termos e condições"
                required
              ></v-checkbox>
              <v-btn type="submit" color="primary" class="mr-4">Cadastrar</v-btn>
              <v-btn color="error">Cancelar</v-btn>
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
      nome: "",
      email: "",
      sexo: "",
      nascimento: "",
      cpf: "",
      telefone: "",
      setor: "",
      matricula: "",
      termos: false
    };
  },
  methods: {
    submit() {
      console.log("Formulário enviado!");
    }
  }
};
</script>