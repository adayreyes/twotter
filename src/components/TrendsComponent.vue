<template>
<div class="input-container">
    <img src="../assets/img/search-12-64.ico" alt="">
    <input type="text" placeholder="Twitter durchsuchen">
</div>
<section class="trends-container">
    <h2>Trends für dich</h2>
    <TrendElement v-for="trend in trends" :trend="trend"/>
</section>
</template>


<script>
import TrendElement from "./TrendElement.vue"
    export default{
        name: "TrendsComponent",
        components: {
            TrendElement
        },
        data(){
            return{
                trends: [
                    {country:"USA",title:"Tesla",quantity:"321000"},
                    {country:"Deutschland",title:"Unwetter",quantity:"6000"},
                    {country:"Spain",title:"Playa",quantity:"54200"},
                    {country:"Österreich",title:"9EuroTicket",quantity:"4000"},
                ]
            }
        }
    }
</script>


<style scoped>

    .trends-container{
        background-color: #EFF1F1;
        padding: 1rem;
        border-radius: 10px;
        width: 300px
    }
    .input-container{
        display: flex;
        align-items: center ;
        gap: 1rem;
        margin-bottom: 2rem;
        background-color: #EFF3F4;
        padding: .5rem;
        border-radius: 99px;
    }

    input{
        border: none;
        background-color: inherit;
        font-size: 1.05rem;

    }

    input:focus{
        outline: none;
    }
    img{
        width: 20px;
    }

  
</style>