<template>
    <div class="header-container">
        <img class="user-img" :src="'src/assets/img/' + userImg" alt="">
        <div class="text-container">
            <div class="user-info">
                <span class="bold">{{name}}</span>
                <span>{{user}}</span>
            </div>
            <p>{{content}}</p>
        </div>
    </div>
    <img class="content-img" :src="'src/assets/img/' + img" alt="">
</template>

<style scoped>
    .header-container{
        display: flex;
        gap: .5rem;
    }
     .user-img{
        width: 40px;
        height: 40px;
        background-color: red;
        border-radius: 100%;
        padding: .5rem;
    }

    .user-info{
        display: flex;
        gap: .3rem;
    }
    .text-container{
        display: flex;
        flex-direction: column;
    }

    .content-img{
        width: 400px;
    }
</style>

<script>
    export default{
        name: "TweetElement",
        props: ["name","user","content","userImg","img"]
    }
</script>