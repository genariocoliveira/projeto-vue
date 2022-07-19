<template>
    <div>
        <h1>Olá, Vue!</h1>
        <h3>Meu nome é: {{ nome }}, e trabalho como {{profissao}}</h3>
    </div>
</template>

<script>
export default {
    name: 'PrimeiroComponente',
    data () {
        return {
            nome: 'Genário',
            profissao: 'Desenvolvedor'
        }
    },
}
</script>