<template>
    <div>
        <form action="">
            <h1>Meu formulário:</h1>
            <div>
                <inputText />
            </div>
            <div>
                <inputText />
            </div>
            <div>
                <Submit />
            </div>
        </form>
    </div>
</template>

<script>
    import inputText from './Form/inputText'    
    import Submit from './Form/submit'

    export default {
        name: 'Form',
        components: {
            inputText,
            Submit
        }
    }
</script>