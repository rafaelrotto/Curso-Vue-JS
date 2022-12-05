<template>
    <h1>meu nome é: {{ name }}</h1>    
</template>

<script>

export default {
    name: 'LifeCycle', 
    data(){
        return{
            name: 'Ainda não sei'
        }
    },
    created() {
        setTimeout(() => {
            this.name = 'Matheus'
        }, 2000)
    },
    mounted(){
        setTimeout(() => {
            this.name = 'Rafael'
        }, 3000)
    },
    methods: {
        lifeCycle(){
            
        }
    }
}

</script>