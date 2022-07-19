<template>
    <div>
        <h2>Está é a descrição da pessoa: {{nome}} </h2>
        <Info/>
        <Form/>
    </div>
</template>

<script>
import Info from './info.vue'
import Form from './form.vue'

export default {
    name: "Pessoa",
    data() {
        return {
            nome: "Genário"
        };
    },
    components: { Form, Info }
}
</script>