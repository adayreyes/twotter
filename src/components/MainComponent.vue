<template>

    <section class="input-container">
        <img class="user-img" src="../assets/img/user-6-64.ico" alt="">
        <div class="input-box">
            <input type="text" placeholder="Was gibt's neues?">
            <div class="input-icons">
                <img src="../assets/img/bell-2-64.ico" alt="">
                <img src="../assets/img/bell-2-64.ico" alt="">
                <img src="../assets/img/bell-2-64.ico" alt="">
                <img src="../assets/img/bell-2-64.ico" alt="">
                <img src="../assets/img/bell-2-64.ico" alt="">
            </div>
        </div>
        <button>Twittern</button>
    </section>
    <section class="content">
        <div v-for="tweet in tweets" class="tweet-container">
            <TweetElement :tweet="tweet"/>
        </div>
    </section> 
</template>

<style scoped>
    .input-container{
        display: flex;
        padding: 1rem;
        gap: 1rem;
        border: 1px solid rgba(0, 0, 0, 0.199);
        margin-bottom: .2rem;

    }

    .tweet-container{
        border: 1px solid rgba(0, 0, 0, 0.199);
        padding: 1rem;
        }
    img{
        width: 20px;
    }
    .user-img{
        width: 40px;
        height: 40px;
        background-color: red;
        border-radius: 100%;
        padding: .5rem;
    }

    .input-box{
        display: flex;
        flex-direction: column;
        gap: 2rem;
    }

    .input-icons{
        display: flex;
        justify-content: space-between;
    }

    button{
        font-weight: bold;
        color: white;
        font-size: 1.05rem;
        background-color: var(--blue);
        height: 30px;
        border-radius: 10px;
    }

    .content{
        display: flex;
        flex-direction: column;
        gap: 2rem;
    }

</style>

<script>
import TweetElement from "./TweetElement.vue"
    export default{
        name:"MainComponent",
        components:{
    TweetElement,
    },

    data(){
        return{
            tweets : [
                {name:"Aday Reyes",user:"@adayreeyes",content:"Hoy es un gran dia para celebrar",img:"me2.JPG",userImg:"user-6-64.ico"},
                {name:"Aday Reyes",user:"@adayreeyes",content:"Hoy es un gran dia para celebrar",img:"me2.JPG",userImg:"user-6-64.ico"},
                {name:"Aday Reyes",user:"@adayreeyes",content:"Hoy es un gran dia para celebrar",img:"me2.JPG",userImg:"user-6-64.ico"},
                {name:"Aday Reyes",user:"@adayreeyes",content:"Hoy es un gran dia para celebrar",img:"me2.JPG",userImg:"user-6-64.ico"},
            ]
        }
    }
    }
</script>