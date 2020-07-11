<template>
  <v-row class="pb-8" style="background-color: #F25F29;">
    <v-row style="width: 100%;" class="mt-8 mb-8">
      <v-row style="width: 100%;">
        <v-spacer></v-spacer>
        <h2 style="color:white; font-size: 2.2em;">Portfólio</h2>
        <v-spacer></v-spacer>
      </v-row>
      <v-row style="width: 100%;">
        <v-spacer></v-spacer>
        <span
          style="color:white; text-align:center; font-size: 1.2em;"
        >Que tal dar uma olhada nos nossos eventos?</span>
        <v-spacer></v-spacer>
      </v-row>
    </v-row>
    <!--EVENTOS REALIZADOS-->
    <v-row>
      <v-row style="width: 100%;" class="mt-2 mb-4">
        <v-spacer></v-spacer>
        <h2 style="color:white; font-size: 1.5em;">Eventos realizados</h2>
        <v-spacer></v-spacer>
      </v-row>
      <v-row style="width:100%;">
        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img01.png"
              @click="auxSrc=require('@/assets/sessao05/img01.png'); enableDialog=true;"
              max-width="220"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img02.png"
              @click="auxSrc=require('@/assets/sessao05/img02.png'); enableDialog=true;"
              max-width="220"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>

        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img03.png"
              @click="auxSrc=require('@/assets/sessao05/img03.png'); enableDialog=true;"
              max-width="220"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
      </v-row>
      <v-row style="width:100%;">
        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img04.png"
              @click="auxSrc=require('@/assets/sessao05/img04.png'); enableDialog=true;"
              max-width="280"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img05.png"
              @click="auxSrc=require('@/assets/sessao05/img05.png'); enableDialog=true;"
              max-width="300"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
      </v-row>
    </v-row>
    <!--PARTICIPAÇÃO COM APOIO-->
    <v-row>
      <v-row style="width: 100%;" class="mt-2 mb-4">
        <v-spacer></v-spacer>
        <h2 style="color:white; font-size: 1.5em;">Participação com apoio</h2>
        <v-spacer></v-spacer>
      </v-row>
      <v-row style="width:100%;">
        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img2_01.png"
              @click="auxSrc=require('@/assets/sessao05/img2_01.png'); enableDialog=true;"
              max-width="220"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img2_02.png"
              @click="auxSrc=require('@/assets/sessao05/img2_02.png'); enableDialog=true;"
              max-width="350"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img2_03.png"
              @click="auxSrc=require('@/assets/sessao05/img2_03.png'); enableDialog=true;"
              max-width="220"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
      </v-row>
      <v-row style="width:100%;">
        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img2_04.png"
              @click="auxSrc=require('@/assets/sessao05/img2_04.png'); enableDialog=true;"
              max-width="280"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img2_05.png"
              @click="auxSrc=require('@/assets/sessao05/img2_05.png'); enableDialog=true;"
              max-width="350"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
        <v-col>
          <v-row class="mb-8">
            <v-spacer></v-spacer>
            <v-img
              src="@/assets/sessao05/img2_06.png"
              @click="auxSrc=require('@/assets/sessao05/img2_06.png'); enableDialog=true;"
              max-width="200"
            ></v-img>
            <v-spacer></v-spacer>
          </v-row>
        </v-col>
      </v-row>
    </v-row>
    <v-dialog v-model="enableDialog" :width="auxWidth">
      <v-img :src="auxSrc"></v-img>
    </v-dialog>
  </v-row>
</template>

<script>
export default {
  name: "Sessao04",

  data: () => ({
    enableDialog: false,
    auxSrc: "",
    auxWidth: 400,
    enableCardEventos: false
  })
};
</script>
