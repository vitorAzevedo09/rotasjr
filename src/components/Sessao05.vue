<template>
  <v-row class="pb-8" style="background-color: #5E2D5A;">
    <v-row style="width: 100%;" class="mt-8 mb-8">
      <v-spacer></v-spacer>
      <h2 style="color:white; font-size: 2.2em;">Contato</h2>
      <v-spacer></v-spacer>
    </v-row>
    <v-row>
      <v-col cols="5">
        <v-row class="mb-8">
          <v-spacer></v-spacer>
          <v-img src="@/assets/sessao02/onibus-escolar.png" max-width="180"></v-img>
          <v-spacer></v-spacer>
        </v-row>
      </v-col>
      <v-col cols="7">
        <v-form ref="form" v-model="valid" lazy-validation>
          <v-container>
            <v-row>
              <label for="name" style="color:white; font-size:1.4em;">Nome</label>
            </v-row>
            <v-row>
              <v-col cols="10" class="pl-0 pb-0">
                <v-text-field
                  dark
                  id="name"
                  color="white"
                  outlined
                  v-model="name"
                  :rules="nameRules"
                  placeholder="Digite seu nome"
                  required
                ></v-text-field>
              </v-col>
            </v-row>
            <v-row>
              <label for="email" style="color:white; font-size:1.4em;">Email</label>
            </v-row>
            <v-row>
              <v-col cols="10" class="pl-0 pb-0">
                <v-text-field
                  style="border-color:white;"
                  dark
                  id="email"
                  color="white"
                  outlined
                  v-model="email"
                  :rules="emailRules"
                  placeholder="Digite seu email"
                  required
                ></v-text-field>
              </v-col>
            </v-row>

            <v-row>
              <label for="subject" style="color:white; font-size:1.4em;">Assunto</label>
            </v-row>
            <v-row>
              <v-col cols="10" class="pl-0 pb-0">
                <v-text-field
                  dark
                  id="subject"
                  color="white"
                  outlined
                  v-model="subject"
                  :rules="subjectRules"
                  placeholder="Digite o assunto da mensagem"
                  required
                ></v-text-field>
              </v-col>
            </v-row>
            <v-row>
              <label for="content" style="color:white; font-size:1.4em;">Mensagem</label>
            </v-row>
            <v-row>
              <v-col cols="10" class="pl-0 pb-0">
                <v-textarea
                  dark
                  id="content"
                  outlined
                  color="white"
                  auto-grow
                  :rules="contentRules"
                  clearable
                  placeholder="O que deseja nos falar?"
                  required
                ></v-textarea>
              </v-col>
            </v-row>
            <v-row>
              <v-btn color="white" outlined class="mr-4" @click="validate">Enviar!</v-btn>
              <v-btn color="error" class="mr-4" @click="reset">Reset</v-btn>
            </v-row>
          </v-container>
        </v-form>
      </v-col>
    </v-row>
  </v-row>
</template>

<script>
export default {
  name: "Sessao05",
  data: () => ({
    valid: false,
    auxTextColor1: "color: white;",
    auxTextColor2: "color: #111A46;",
    name: "",
    nameRules: [
      v => !!v || "Você precisa inserir seu nome",
      v => v.length <= 30 || "Seu nome deve possuir menos de 30 caracteres"
    ],
    email: "",
    emailRules: [
      v => !!v || "Você precisa inserir seu e-mail",
      v => /.+@.+/.test(v) || "Você precisa inserir um e-mail válido"
    ],
    subject: "",
    subjectRules: [
      v => !!v || "Você precisa inserir o assunto do email",
      v => v.length <= 30 || "O assunto deve possuir menos de 30 caracteres"
    ],
    content: "",
    contentRules: [v => !!v || "Você precisa inserir o conteúdo do email"]
  }),
  methods: {
    validate() {
      this.$refs.form.validate();
    },
    reset() {
      this.$refs.form.reset();
      this.$refs.form.resetValidation();
    }
  }
};
</script>
