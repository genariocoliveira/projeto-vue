<template>
    <ul>
        <li>
            <a href="#">Homes</a>
        </li>
        <li>
            <a href="#">Service</a>
        </li>
        <li>
            <a href="#">Contact</a>
        </li>
        <li>
            <a href="#">About</a>
        </li>
    </ul>
</template>

<script>
    export default {
        name: 'Header'
    }
</script>

<style scoped>
ul{
    list-style: none;
    display: flex;
    background: #ccc;
}
li{
    margin-right: 10px;
}
a{
    color: rgb(0, 0, 0);
    text-decoration: none;
    transition: ease-in-out 0.5s;
}
a:hover{
    color:tomato;
}

</style>