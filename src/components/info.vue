<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias para Back-end:</p>
        <ul>
            <li v-for="(technology, index) in backend_tech" v-bind:key="index">{{technology}}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias front-end:</p>
        <ul>
            <li v-for="technology in frontend_tech" v-bind:key="technology.id">
                {{technology.language}}
            </li>
        </ul>
        <button @click="ShowEmail">{{ mail }}</button>
        <p v-show="mostrar_email">Mande uma mensagem para: {{email}}</p>
        <p class="teste">Para acessar meu portfólio basta clicar <a v-bind:href="meu_link" target="_blank">aqui</a></p>
        <Picture/>
    </div>
</template>

<script>
import Picture from './Picture.vue'

    export default {
        name: 'Info',
        components: { 
            Picture 
        },
        data() {
            return {
                esta_trabalhando: false,
                mostrar_email: false,
                email: 'genariocdeoliveira@gmail.com',
                meu_link: 'https://google.com',
                mail: 'Mostrar e-mail',
                backend_tech: ['JavaScript', 'PHP', 'Python'],
                frontend_tech: [
                    {id: 1, language: 'HTML'},
                    {id: 2, language: 'CSS'},
                    {id: 3, language: 'Vue'}
                ]
            }
        },
        methods: {
            ShowEmail(){
                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email){
                    this.mail = 'Mostrar e-mail'
                } else {
                    this.mail = 'Ocultar e-mail'
                }
                // O IF significar. Quando o botão mostrar email for falso, aparece o texto MOSTRAR E-MAIL, quando for verdadeira mostra o texto OCULTAR E-MAIL
            }
        }
    }
</script>