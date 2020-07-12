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
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d7969.355079402552!2d-41.75786412353776!3d-2.9088561780278237!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x7ec255a0bc46b2d%3A0x934a4feacf90f37b!2sRotas%20-%20Empresa%20J%C3%BAnior%20de%20Turismo!5e0!3m2!1sen!2sbr!4v1594472730576!5m2!1sen!2sbr"
                frameborder="0"
                style="border:0;"
                allowfullscreen=""
                aria-hidden="false"
                tabindex="0"
              ></iframe>
        </v-row>
      </v-col>
      <v-col cols="7">
        <v-form ref="form" v-model="valid" lazy-validation>
          <v-container>
            <v-row>
              <label for="name" style="color:white; font-size:1.4em;"
                >Nome</label
              >
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
              <label for="email" style="color:white; font-size:1.4em;"
                >Email</label
              >
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
              <label for="subject" style="color:white; font-size:1.4em;"
                >Assunto</label
              >
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
              <label for="content" style="color:white; font-size:1.4em;"
                >Mensagem</label
              >
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
              <v-btn color="white" outlined class="mr-4" @click="validate"
                >Enviar!</v-btn
              >
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
    rotas_src:
      "https://maps.google.com/maps?q=rotas%20jr&t=&z=13&ie=UTF8&iwloc=&output=embed",
    auxTextColor1: "color: white;",
    auxTextColor2: "color: #111A46;",
    name: "",
    nameRules: [
      (v) => !!v || "Você precisa inserir seu nome",
      (v) => v.length <= 30 || "Seu nome deve possuir menos de 30 caracteres",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "Você precisa inserir seu e-mail",
      (v) => /.+@.+/.test(v) || "Você precisa inserir um e-mail válido",
    ],
    subject: "",
    subjectRules: [
      (v) => !!v || "Você precisa inserir o assunto do email",
      (v) => v.length <= 30 || "O assunto deve possuir menos de 30 caracteres",
    ],
    content: "",
    contentRules: [(v) => !!v || "Você precisa inserir o conteúdo do email"],
  }),
  methods: {
    validate() {
      this.$refs.form.validate();
    },
    reset() {
      this.$refs.form.reset();
      this.$refs.form.resetValidation();
    },
  },
};
</script>
<style lang="css" slot-scoped>

iframe {
  width: 50vw;
  height: 50vh;
  padding:3vw;
}
</style>
