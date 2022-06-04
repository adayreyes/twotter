<template>
    <div>
        <img :src="'src/assets/img/' + img" alt="">
        <span>{{title}}</span>
    </div>
</template>

<style scoped>
    @import url(../assets/css/nav-element.css);
</style>

<script>
    export default{
        name: "NavElement",
        props: ["title","img"]
    }
</script>
