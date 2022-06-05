<template>
    <div>
        <img :src="'src/assets/img/' + img" alt="">
        <span>{{title}}</span>
    </div>
</template>

<style scoped>
    div{
    display: flex;
    gap: 1rem;
    
    }
    img{
    width: 30px;
    }
</style>

<script>
    export default{
        name: "NavElement",
        props: ["title","img"]
    }
</script>
