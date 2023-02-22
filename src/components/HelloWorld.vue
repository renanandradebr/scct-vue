<template>
  <v-container>
    <div>
      <v-breadcrumbs divider="\">Dashboard \</v-breadcrumbs>
    </div>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img :src="require('../assets/logo-scct.png')" class="my-8 " contain height="100" />
      </v-col>

    </v-row>


    <v-divider></v-divider>
    <v-row>

      <v-col cols="4" class="pa-4 my-4">
        <v-container>
          <v-row justify="center">

            <v-btn block color="primary" class="mb-2" to='./cadastro' elevation="1" outlined>CADASTRO DE USUÁRIO</v-btn>


            <v-spacer></v-spacer>

            <v-btn block color="primary" class="mb-2" to='./cadastroTelefone' elevation="1" outlined>TELEFONE FIXO</v-btn>

            <v-spacer></v-spacer>

            <v-btn block color="primary" class="mb-2" elevation="1" outlined>TELEFONE
              CELULAR</v-btn><v-spacer></v-spacer>

            <v-btn block color="primary" class="mb-2" elevation="1" outlined>AGENDA TELEFÔNICA</v-btn>

            <v-btn block color="primary" class="mb-2" elevation="1" outlined>SOLICITAR BACKUPS</v-btn>

            <v-btn block color="primary" class="mb-2" elevation="1" outlined>ACESSAR LOGS DE USUÁRIO</v-btn>
          </v-row>
        </v-container>
      </v-col>

      <v-col cols="8">
        <div class="carousel-container">
          <v-carousel hide-delimiters cycle height="400" style="max-width: 600px; margin: 0 auto;">
            <v-carousel-item v-for="item in items" :key="item.title" :src="item.image">
              <v-sheet color="primary" dark class="pa-2" absolute bottom left style="max-width: 70%">
                <div class="headline white--text mb-3">{{ item.title }}</div>
                <div class="body-2 white--text">{{ item.description }}</div>
              </v-sheet>
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
          title: "Nova tecnologia ajuda a reduzir o desperdício de água em São Paulo",
          description:
            "Uma nova tecnologia desenvolvida por pesquisadores da USP permite a detecção de vazamentos em tubulações de água, reduzindo o desperdício do recurso. O projeto-piloto já está em andamento na cidade de São Paulo.",
          image: "https://via.placeholder.com/800x400/00b8d4/ffffff",
        },
        {
          title: "Crise hídrica em Brasília: governador anuncia racionamento de água",
          description:
            "Com a falta de chuvas na região, o governo do Distrito Federal anunciou um plano de racionamento de água. A medida entrará em vigor na próxima semana e irá afetar mais de 1 milhão de pessoas.",
          image: "https://via.placeholder.com/800x400/f4511e/ffffff",
        },
        {
          title: "Novo sistema de captação de água de chuva é inaugurado no Rio de Janeiro",
          description:
            "Um novo sistema de captação de água de chuva foi inaugurado hoje na cidade do Rio de Janeiro. O equipamento, instalado em uma escola pública, tem capacidade para armazenar até 10 mil litros de água e será utilizado para irrigar a horta da instituição.",
          image: "https://via.placeholder.com/800x400/4caf50/ffffff",
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
  /* Aqui você pode definir a margem desejada */
}
</style>