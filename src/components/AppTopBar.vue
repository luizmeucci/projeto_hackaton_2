<template>
    <div class=app-top-bar>
            <v-app-bar color="green" dense dark>
            <v-app-bar-nav-icon @click="drawer = true" ></v-app-bar-nav-icon>
            <v-toolbar-title>Coleta seletiva de lixo</v-toolbar-title>
            </v-app-bar>
            <v-navigation-drawer
            v-model="drawer"
            absolute
            temporary
            >
            <v-list
                nav
                
            >
                <v-list-item-group
                v-model="group"
                color="white"
                active-class="green--text text--darken-1">
                <router-link to="/">
                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>mdi-home</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Início</v-list-item-title>
                </v-list-item>
                </router-link>

                <router-link to="/PontosColeta">
                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>mdi-delete</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Pontos de coleta</v-list-item-title>
                </v-list-item>
                </router-link>

                <router-link to="/informacoes">
                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>mdi-information-outline</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Informações</v-list-item-title>
                </v-list-item>
                </router-link>

                <router-link to="/compostagem">
                <v-list-item>
                    <v-list-item-icon>
                    <v-icon>mdi-leaf</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Compostagem</v-list-item-title>
                </v-list-item>
                </router-link>

                </v-list-item-group>
            </v-list>
            </v-navigation-drawer>

    </div>
</template>

<script>
export default {
    name: 'AppTopBar',
    data: () => ({
                 drawer: false,
                 group: null,
  }),
}
</script>

<style scoped>
.app-top-bar a{
text-decoration: none;
}
</style>