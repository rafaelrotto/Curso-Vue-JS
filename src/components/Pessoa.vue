<template>
  <div>
    <h2>Está é a descrição da pessoa: {{ name }}</h2>
    <info :email="email"/>
    <Form />
  </div>
</template>

<script>
import Form from './form.vue'
import info from './info.vue'
    export default {
  components: { info },
        name: 'Pessoa',
        components: {
            info, Form
        },
        data(){
            return{
                name: 'Matheus',
                email: 'rafael@gmail.com'
            }
        }
    }
</script>