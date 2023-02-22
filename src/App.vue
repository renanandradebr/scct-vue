<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img alt="scct-logo" class="shrink mx-3" contain src="./assets/logo-scct2.png" transition="scale-transition"
          width="110" />

        <v-btn class="mr-2" to='./' color="primary">home</v-btn>

        <v-btn class="mr-2" color="primary">backups</v-btn>
   
          <v-btn class="mr-2" to='./contatos' color="primary">Contatos</v-btn>

        <v-btn class="mr-2" color="primary">Opções</v-btn>
      </div>
      <div>
        <v-list-item to="/loginPage">
          <v-list-item-icon>
            <v-icon>mdi-login</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Login</v-list-item-title>
        </v-list-item>
      </div>

      <v-spacer></v-spacer>

    </v-app-bar>
    <v-main>

      <router-view />
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
