<template>
    <div>
        <ul>
            <li><a href="#">HOME</a></li>
            <li><a href="#">PROJETOS</a></li>
            <li><a href="#">CONTATO </a></li>
        </ul>

    </div>
</template>

<script>
    export default {
        name : 'HeaderComponente'
    }

</script>

<style scoped>
    ul {
        list-style: none;
        display: flex;
    }

    li {
        margin-right: 10px;
    }

    a {
        color: #DDD;
        text-decoration: none;
        transition: .5s;
    }

    a:hover {
        color: turquoise;
    }
</style>>

