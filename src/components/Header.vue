<template>
    <ul>
        <li><a href ="#">Home</a></li>
    </ul>
</template>
<script>
export default {
    name: "Header"
}
</script>

<style scoped>
ul{
    list-style: none;
    display: flex;
    background: #c6d9db;
}

li {
    margin-right: 10px;
}

a{
    color: #021842;;
    text-decoration: none;
    transition: .5s;
}

a:hover{
    color: #1ae4ff;
}
</style>