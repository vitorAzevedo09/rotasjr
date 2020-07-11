<template>
  <v-app>
    <v-app-bar app color="white" dark height="100">
      <v-spacer></v-spacer>
      <div class="d-flex align-center">
        <v-img
          alt="Rotasjr Logo"
          contain
          src="@/assets/logo_rotas.png"
          transition="scale-transition"
          width="180"
        />
      </div>

      <v-btn v-for="(item, i) in menu_items" text :key="i">
        <span class="mr-2" style="color:black;">{{item.title}}</span>
      </v-btn>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-content>
      <Sessao01 />
    </v-content>
  </v-app>
</template>

<script>
import Sessao01 from "./components/Sessao01.vue";

export default {
  name: "App",

  components: {
    Sessao01
  },

  data: () => ({
    menu_items: [
      { title: "Home", src: null },
      { title: "Nossos Serviços", src: null },
      { title: "Quem somos", src: null },
      { title: "Portfólio", src: null },
      { title: "Contato", src: null }
    ]
  })
};
</script>
