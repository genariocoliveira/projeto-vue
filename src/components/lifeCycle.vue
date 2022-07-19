<template>
    <h1>My name is: {{ nome }}</h1>
</template>

<script>
    export default {
        name: 'lifeCycle',
        data() {
            return{
                nome: 'Ainda não sei...'
            }
        },
        created() {
            setTimeout(()=>{
                this.nome = 'Genário'
            },2000);
            this.lifeCycle()
        },
        mounted() {
            setTimeout(()=>{
                this.nome = 'Rebeca'
            },2000);
            this.lifeCycle()
        },
        methods: {
            lifeCycle() {
                console.log('Executou!!!')
            }
        }
    }
</script>