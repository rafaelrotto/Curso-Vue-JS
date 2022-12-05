<template>
  <div>
    <p>{{ email }}</p>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes tecnologias para Back-end:</p>
    <ul>
      <li
        v-for="(technology, index) in backend_technologies"
        v-bind:key="index"
      >
        {{ technology }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para o Front-end</p>
    <ul>
      <li v-for="technology in frontend_technologies" :key="technology.id">
        {{ technology.language }}
      </li>
    </ul>
    <div>
      <button @click="showEmail">{{ texto_botao }}</button>
    </div>
    <p v-show="mostrar_email">mande uma mensagem para: {{ email }}</p>
    <p>Para acessar meu portifólio</p>
    <a v-bind:href="meu_link" target="blank">basta clicar aqui</a>
    <Picture />
  </div>
</template>

<script>
import Picture from "./Picture.vue";
export default {
  components: { Picture },
  name: "info",
  props:{
    email: String
  },
  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      meu_link: "https://google.com",
      texto_botao: "Mostrar Email",
      backend_technologies: ["Java", "PHP", "C", "JavaScript"],
      frontend_technologies: [
        { id: 1, language: "HTML" },
        { id: 2, language: "CSS" },
        { id: 3, language: "Vue" },
      ],
    };
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.texto_botao = "Mostrar Email";
      } else {
        this.texto_botao = "Ocultar Email";
      }
    },
  },
};
</script>