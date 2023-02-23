<template>
    <v-app>
        <v-navigation-drawer app v-model="drawer">
            <v-list>
                <v-list-item v-for="(item, index) in items" :key="index" @click="selectItem(item)">
                    <v-list-item-action>
                        <v-icon>{{ item.icon }}</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
        <v-app-bar app>
            <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title>{{ selected }}</v-toolbar-title>
        </v-app-bar>
        <v-main>
            <v-container fluid>
                <router-view></router-view>
            </v-container>
        </v-main>
    </v-app>
</template>

<script>
export default {
    data() {
        return {
            drawer: false,
            selected: "",
            items: [
                { title: "Home", icon: "mdi-home", link: "/" },
                { title: "Perfil", icon: "mdi-account", link: "/perfil" },
                { title: "Configurações", icon: "mdi-cog", link: "/config" }
            ]
        };
    },
    methods: {
        selectItem(item) {
            this.selected = item.title;
            this.$router.push(item.link);
        }
    }
};
</script>