<template>
    <section class="nav-container">
        <img src="../assets/img/twitter-64.ico" alt="">
        <NavElement v-for="route in routes" :title="route.title" :img = "route.img"/>
    </section>
    <section class="user-container">
        <img src="../assets/img/user-6-64.ico" alt="">
        <div class="user-info">
            <span>Aday Reyes</span>
            <span>@adayreeyes</span>
        </div>
        <img src="../assets/img/settings-3-64.ico" alt="">
    </section>
</template>
<style scoped>

    .nav-container{
        display: flex;
        flex-direction: column;
        gap: 1rem;
        font-size: 1.2rem;
    }

    .nav-container img{
        width: 40px;
    }

    .user-container{
        display: flex;
        gap: 1rem;

    }
    .user-container img{
        width: 40px;
        height: 40px;
        border-radius: 100%;
    }
    .user-container .user-info{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>
<script>
import NavElement from "./NavElement.vue";

export default{
    name: "HeaderComponent",
    components: {
        NavElement
    },
    data() {
        return {
            routes : [
                {title:"Start",img:"home-3-64.ico"},
                {title:"Notifications",img:"bell-2-64.ico"},
                {title:"Messages",img:"email-5-64.ico"},
                {title:"Profile",img:"user-6-64.ico"},
                {title:"Settings",img:"settings-3-64.ico"}
            ]

        }
    }
    
    
}

</script>