<template>
  <v-app>
    <v-app-bar app color="white" dark height="100">
      <v-spacer></v-spacer>
      <v-app-bar-nav-icon
        class="hidden-md-and-up"
        color="purple"
        @click.stop="drawer = !drawer"
      ></v-app-bar-nav-icon>
      <v-toolbar-title>
        <div class="d-flex align-center">
          <v-img
            alt="Rotasjr Logo"
            contain
            src="@/assets/logo_rotas.png"
            transition="scale-transition"
            width="180"
          />
        </div>
      </v-toolbar-title>
      <v-toolbar-item class="hidden-sm-and-down">
        <v-btn
          v-for="(item, i) in menu_items"
          text
          :key="i"
          class="float-sm-left"
          @click="
            $vuetify.goTo(item.src, {
              duration: 1000,
              offset: 0,
              easing: 'easeInOutCubic',
            })
          "
          style="width:8%;"
          min-width="150"
        >
          <span class="mr-2" style="color:black;font-size:100%;">{{
            item.title
          }}</span>
        </v-btn>
      </v-toolbar-item>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer"  app temporary>
      <v-list nav dense>
        <v-list-item-group active-class="deep-purple--text text--accent-4">
          <v-list-item
            v-for="(item, i) in menu_items"
            :key="i"
            @click="
              $vuetify.goTo(item.src, {
                duration: 1000,
                offset: 0,
                easing: 'easeInOutCubic',
              });drawer= !drawer
            "
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title >{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-content>
      <Sessao01 id="Sessao01" />
      <Sessao02 id="Sessao02" />
      <Sessao03 id="Sessao03" />
      <Sessao04 id="Sessao04" />
      <Sessao05 id="Sessao05" />
      <Sessao06 id="Sessao06" />
    </v-content>
  </v-app>
</template>

<script>
import Sessao01 from "./components/Sessao01.vue";
import Sessao02 from "./components/Sessao02.vue";
import Sessao03 from "./components/Sessao03.vue";
import Sessao04 from "./components/Sessao04.vue";
import Sessao05 from "./components/Sessao05.vue";
import Sessao06 from "./components/Sessao06.vue";

import { mdiAccountGroup, mdiFolderMarker, mdiCellphoneMessage } from "@mdi/js";

export default {
  name: "App",

  components: {
    Sessao01,
    Sessao02,
    Sessao03,
    Sessao04,
    Sessao05,
    Sessao06,
  },

  data: () => ({
    menu_items: [
      { title: "Home", src: "#Sessao01", icon:"mdi-home" },
      { title: "Nossos Serviços", src: "#Sessao02", icon:"mdi-room-service" },
      { title: "Quem somos", src: "#Sessao03", icon: mdiAccountGroup },
      { title: "Portfólio", src: "#Sessao04", icon: mdiFolderMarker },
      { title: "Contato", src: "#Sessao05", icon: mdiCellphoneMessage },
    ],
    drawer: false,
  }),
};
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Montserrat");

#app {
  font-family: "Montserrat";
}
</style>
