<template>
  <v-row class="pb-8" style="background-color: #5E2D5A;">
    <v-row>
      <v-col cols="5">
        <v-row class="mb-8">
          <v-spacer></v-spacer>
            <v-img
              alt="Rotasjr Logo"
              contain
              src="@/assets/logo_rotas.png"
              transition="scale-transition"
              style="width:20em"
            />
          <v-spacer></v-spacer>
        </v-row>
      </v-col>
      <v-col cols="7">
        <v-row>
          <v-col>
            <h2 style="color:white; font-size: 2.2em;">Social</h2>
          </v-col>
          <v-col>
            <h2 style="color:white; font-size: 2.2em;">Telefone</h2>
          </v-col>
          <v-col>
            <h2 style="color:white; font-size: 2.2em;">Email</h2>
          </v-col>
        </v-row>
        <v-row>
          <v-col
            @click="$route.push('https://www.facebook.com/empresajrrotas')"
          >
            <a
              href="https://www.facebook.com/empresajrrotas"
              style="text-decoration: none;"
            >
              <v-icon size="50" color="white">mdi-facebook</v-icon
              ><span style="color:white; font-size: 1.5em;padding:1em;"
                >empresajrrotas</span
              >
            </a>
          </v-col>
          <v-col>
            <h2 style="color:white; font-size: 1.5em;">(086) 9 9480-8620</h2>
          </v-col>
          <v-col>
            <a
              href="mailto:empresajrrotas@gmail.com"
              style="text-decoration: none;"
            >
            <v-icon size="40" color="white">mdi-email</v-icon>
            <span style="color:white; font-size: 1em;">
              empresajrrotas@gmail.com
            </span>
            </a>
          </v-col>
        </v-row>
        <v-row>
          <v-col>
            <a
              href="https://www.instagram.com/rotasjr/"
              style="text-decoration: none;"
            >
              <v-icon size="50" color="white">mdi-instagram</v-icon
              ><span style="color:white; font-size: 1.5em;padding:1em;"
                >rotasjr</span
              >
            </a>
          </v-col>
          <v-col>
            <v-row
              ><h2 style="color:white; font-size: 1.5em;">
                Localização
              </h2></v-row
            >
            <v-row>
              <v-col col="1">
                <v-icon color="white" size="70">{{ place }}</v-icon>
              </v-col>
              <v-col cols="10">
                <h2 style="color:white; font-size: 1em;">
                  Avenida São Sebastião,2819.<br />
                  Bloco:03, Sala: 05. UFPI-CMRV<br />
                  Bairro São Benedito, Parnaíba-PI.
                </h2>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-row>
</template>

<script>
import { mdiMapMarkerRadiusOutline } from "@mdi/js";

export default {
  name: "Sessao06",
  data() {
    return {
      place: mdiMapMarkerRadiusOutline,
    };
  },
};
</script>
