<template>
  <v-row class="pb-8" style="background-color: #5E2D5A;">
    <v-row style="width: 100%;" class="mt-8 mb-8">
      <v-spacer></v-spacer>
      <h2 style="color:white; font-size: 2.2em;">Nossos Serviços</h2>
      <v-spacer></v-spacer>
    </v-row>
    <v-row>
      <v-col>
        <v-row class="mb-6">
          <v-spacer></v-spacer>
          <h3 style="color:white;">Agenciamento e transportes</h3>
          <v-spacer></v-spacer>
        </v-row>
        <v-row class="mb-8">
          <v-spacer></v-spacer>
          <v-img src="@/assets/sessao02/onibus-escolar.png" max-width="180"></v-img>
          <v-spacer></v-spacer>
        </v-row>
        <v-row class="mb-8">
          <v-spacer></v-spacer>
          <span style="color:white; font-size: 2.0em;">V</span>
          <v-spacer></v-spacer>
        </v-row>
      </v-col>
      <v-col>
        <v-row class="mb-6" v-if="!enableCardEventos">
          <v-spacer></v-spacer>
          <h3 style="color:white;">Eventos</h3>
          <v-spacer></v-spacer>
        </v-row>
        <v-row class="mb-8" v-if="!enableCardEventos">
          <v-spacer></v-spacer>
          <v-img src="@/assets/sessao02/calendario.png" max-width="180"></v-img>
          <v-spacer></v-spacer>
        </v-row>
        <v-row class="mb-8" v-if="!enableCardEventos">
          <v-spacer></v-spacer>
          <v-btn text style="color: white; font-size: 2.0em;" @click="enableCardEventos=true">V</v-btn>
          <v-spacer></v-spacer>
        </v-row>
        <v-row v-if="!enableCardEventos">
          <v-spacer></v-spacer>
          <v-btn class="mb-2" outlined x-large color="white" width="60%">Fale conosco!</v-btn>
          <v-spacer></v-spacer>
        </v-row>
        <v-card class="mx-auto mb-8" max-width="344" v-if="enableCardEventos" elevation="20">
          <v-card-text>
            <v-row class="mb-10">
              <v-spacer></v-spacer>
              <h3 style="color:#5E2D5A; font-size: 1.4em;">Eventos</h3>
              <v-spacer></v-spacer>
            </v-row>
            <v-row class="mb-12">
              <v-spacer></v-spacer>
              <v-img src="@/assets/sessao02/calendario.png" max-width="180"></v-img>
              <v-spacer></v-spacer>
            </v-row>
            <v-row class="mb-6">
              <v-spacer></v-spacer>
              <ul style="list-style-type: none; width:100%;">
                <li style="color: #5E2D5A; font-size: 1.1em;" class="mb-2">
                  <v-spacer></v-spacer>
                  <h3>
                    <v-icon x-small color="#5E2D5A" class="mr-2">mdi-checkbox-blank-circle</v-icon>
                    <span class="mr-4">Programação de Eventos</span>
                  </h3>
                  <v-spacer></v-spacer>
                </li>
                <li style="color: #5E2D5A; font-size: 1.1em;" class="mb-2">
                  <h3>
                    <v-icon x-small color="#5E2D5A" class="mr-2">mdi-checkbox-blank-circle</v-icon>
                    <span class="mr-6">Organização</span>
                  </h3>
                </li>
                <li style="color: #5E2D5A; font-size: 1.1em;" class="mb-2">
                  <h3>
                    <v-icon x-small color="#5E2D5A" class="mr-2">mdi-checkbox-blank-circle</v-icon>
                    <span class="mr-6">Captação</span>
                  </h3>
                </li>
              </ul>
              <v-spacer></v-spacer>
            </v-row>
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn text style="color: #5E2D5A; font-size: 3.5em;" @click="enableCardEventos=false">^</v-btn>
            <v-spacer></v-spacer>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col>
        <v-row class="mb-6">
          <v-spacer></v-spacer>
          <h3 style="color:white;">Desenvolvimento regional e Turístico</h3>
          <v-spacer></v-spacer>
        </v-row>
        <v-row class="mb-8">
          <v-spacer></v-spacer>
          <v-img src="@/assets/sessao02/bussola.png" max-width="180"></v-img>
          <v-spacer></v-spacer>
        </v-row>
        <v-row class="mb-8">
          <v-spacer></v-spacer>
          <span style="color:white; font-size: 2.0em;">V</span>
          <v-spacer></v-spacer>
        </v-row>
      </v-col>
    </v-row>
  </v-row>
</template>

<script>
export default {
  name: "Sessao02",

  data: () => ({
    enableCardEventos: false
  })
};
</script>
