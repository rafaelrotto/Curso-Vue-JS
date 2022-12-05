<template>
  <div>
    <h1>Olá Vue!</h1>
    <p>meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
    <MultiplosEventos />
    <Reutilizacao />
  </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue';
import Reutilizacao from './Reutilizacao.vue';

export default {
    name: "PrimeiroComponente",
    data() {
        return {
            nome: "Matheus",
            profissao: "Programador"
        };
    },
    components: { MultiplosEventos, Reutilizacao }
};
</script>