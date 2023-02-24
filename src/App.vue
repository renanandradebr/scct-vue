<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img alt="scct-logo" class="shrink mx-3" contain src="./assets/logo-scct2.png" transition="scale-transition"
          width="110" />

        <v-btn class="mr-2" to='./' color="primary"><v-icon>mdi-home</v-icon>HOme</v-btn>

        <v-btn class="mr-2" color="primary"><v-icon>mdi-cloud-upload</v-icon>backups</v-btn>

        <v-btn class="mr-2" to='./contatos' color="primary"><v-icon>mdi-contacts</v-icon>Contatos</v-btn>

      
      </div>


      <v-spacer></v-spacer>

      <div>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      </div>
    </v-app-bar>

    <v-navigation-drawer app right color="blue darken-2" v-model="drawer">

      <div>
        <v-list-item style="color:antiquewhite" to="/loginPage">
          <v-list-item-icon>
            <v-icon style="color: antiquewhite;">mdi-login</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Login</v-list-item-title>
        </v-list-item>
      </div>

      <div>
        <v-list-item style="color:antiquewhite" to="/contatos">
          <v-list-item-icon>
            <v-icon style="color: antiquewhite;">mdi-account</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Contatos</v-list-item-title>
        </v-list-item>
      </div>
      <div>
        <v-list-item style="color:antiquewhite" to="/opções">
          <v-list-item-icon>
            <v-icon style="color: antiquewhite;">mdi-cog</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Configurações</v-list-item-title>
        </v-list-item>
      </div>



    </v-navigation-drawer>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data() {
    return {
      drawer: false
    }
  },
};
</script>
