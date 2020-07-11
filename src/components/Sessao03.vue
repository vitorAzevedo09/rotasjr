<template>
  <v-row>
    <!-- QUEM SOMOS -->
    <v-row class="pb-8" style="background-color: white;">
      <v-row style="width: 100%;" class="mt-8 mb-8">
        <v-row style="width: 100%;" class="mb-4">
          <v-spacer></v-spacer>
          <h2 style="color:#5E2D5A; font-size: 2.2em;">Quem somos</h2>
          <v-spacer></v-spacer>
        </v-row>
        <v-row style="width: 100%;">
          <v-spacer></v-spacer>
          <span style="color:#5E2D5A; text-align:center;">
            Somos a empresa júnior de turismo na Universidade Federal do Piauí.
            <br />Atuando no presente momento na cidade de Parnaíba-PI
          </span>
          <v-spacer></v-spacer>
        </v-row>
      </v-row>
      <v-row>
        <v-col>
          <v-row class="mb-6">
            <v-spacer></v-spacer>
            <h3 style="color:#5E2D5A; font-size: 2.0em;">Missão</h3>
            <v-spacer></v-spacer>
          </v-row>
          <v-row class="mb-12">
            <v-spacer></v-spacer>
            <v-img src="@/assets/sessao03/alvo.png" max-width="180"></v-img>
            <v-spacer></v-spacer>
          </v-row>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <span style="color: #5E2D5A; text-align:center;">
              Elaborar atividades de consultoria e prestar
              <br />serviços no âmbito do turismo regional, <br />objetivando
              contribuir socialmente <br />para o desenvolvimento local.
            </span>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
        <v-col>
          <v-row class="mb-6">
            <v-spacer></v-spacer>
            <h3 style="color:#5E2D5A;  font-size: 2.0em;">Visão</h3>
            <v-spacer></v-spacer>
          </v-row>
          <v-row class="mb-12">
            <v-spacer></v-spacer>
            <v-img src="@/assets/sessao03/visao.png" max-width="180"></v-img>
            <v-spacer></v-spacer>
          </v-row>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <span style="color: #5E2D5A; text-align:center;">
              Tornar-se uma empresa reconhecida
              <br />em seu trabalho com excelência <br />em consultoria, eventos
              e no <br />desenvolvimento do Turismo em <br />todo o estado do
              Piauí.
            </span>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
        <v-col>
          <v-row class="mb-6">
            <v-spacer></v-spacer>
            <h3 style="color:#5E2D5A; font-size: 2.0em;">Valores</h3>
            <v-spacer></v-spacer>
          </v-row>
          <v-row class="mb-12">
            <v-spacer></v-spacer>
            <v-img src="@/assets/sessao03/valor.png" max-width="180"></v-img>
            <v-spacer></v-spacer>
          </v-row>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <span style="color: #5E2D5A; text-align:center;">
              A empresa busca atuar no mercado
              <br />sempre com ética, responsabilidade, <br />profissionalismo e
              respeito, levando <br />em consideração o espírito empreendedor.
            </span>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
      </v-row>
    </v-row>

    <!-- EQUIPE -->

    <v-row class="pb-12 mb-8" style="background-color: white;">
      <v-row style="width: 100%;" class="mt-8 mb-8">
        <v-row style="width: 100%;" class="mb-2">
          <v-spacer></v-spacer>
          <h2 style="color:#5E2D5A; font-size: 3em;">Equipe</h2>
          <v-spacer></v-spacer>
        </v-row>
        <v-row style="width: 100%;">
          <v-spacer></v-spacer>
          <span style="color:#5E2D5A; text-align:center; font-size: 1.5em;"
            >Aqueles que fazem tudo funcionar!</span
          >
          <v-spacer></v-spacer>
        </v-row>
      </v-row>
      <v-row class="ml-12">
        <v-col v-for="(person, i) in persons" :key="i" cols="2">
          <v-spacer></v-spacer>
          <v-hover v-slot:default="{ hover }">
            <v-card max-width="250" class="grow" :elevation="hover ? 16 : 2">
              <v-img
                v-if="person.imgURL !== ''"
                :src="require(`@/assets/sessao04/${person.imgURL}`)"
                max-width="250"
              >
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out purple  darken-2 v-card--reveal white--text"
                    style="height: 30%;position:relative;bottom:-70%;"
                  > <span style="width:70%;padding:auto;margin:auto;font-size:1vw;">{{ person.role }}<br>
                    {{ person.name }}</span>
                    
                  </div>
                </v-expand-transition>
                <v-row
                  v-if="!hover"
                  class="d-flex transition-fast-in-fast-out purple darken-2 v-card--reveal white--text"
                  style=" height:100%; background-color: #5E2D5A;  opacity: 0.5;"
                ></v-row>
              </v-img>
              <v-img
                v-else
                src="@/assets/sessao04/conta.png"
                max-width="230"
                style="width:10vw;"
              >
                <v-row
                  style=" height:100%; background-color: #5E2D5A;  opacity: 0.5;"
                ></v-row>
              </v-img>
            </v-card>
          </v-hover>
          <v-spacer></v-spacer>
        </v-col>
      </v-row>
    </v-row>
  </v-row>
</template>

<script>
export default {
  name: "Sessao03",

  data: () => ({
    teste: false,
    persons: [
      {
        imgURL: "arlindo-oliveira.png",
        name: "Arlindo Oliveira",
        role: "Presidente",
      },
      {
        imgURL: "solano-braga.png",
        name: "Solano Braga",
        role: "Vice-Presidente",
      },
      {
        imgURL: "arlindo-oliveira.png",
        name: "Arlindo Oliveira",
        role: "Presidente",
      },
      {
        imgURL: "solano-braga.png",
        name: "Solano Braga",
        role: "Vice-Presidente",
      },
      {
        imgURL: "arlindo-oliveira.png",
        name: "Arlindo Oliveira",
        role: "Presidente",
      },
      {
        imgURL: "solano-braga.png",
        name: "Solano Braga",
        role: "Vice-Presidente",
      },
      {
        imgURL: "arlindo-oliveira.png",
        name: "Arlindo Oliveira",
        role: "Presidente",
      },
      {
        imgURL: "solano-braga.png",
        name: "Solano Braga",
        role: "Vice-Presidente",
      },
      {
        imgURL: "",
      },
      {
        imgURL: "",
      },
      {
        imgURL: "",
      },
    ],
  }),
};
</script>
<style scoped>


@media only screen and (min-width: 600px) {
  .grow {
  transition: 1s ease;
}

.grow:hover {
  -webkit-transform: scale(1.15);
  -ms-transform: scale(1.15);
  transform: scale(1.15);
  transition: 0.6s ease;
}
}
</style>
