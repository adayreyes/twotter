<template>
     <div class="trend-box">
        <div class="trend-info">
            <span>Trend in {{trend.country}}</span>
            <span class="bold">{{trend.title}}</span>
            <span>{{trend.quantity}} Tweets</span>
        </div>
        <span class="more-icon">...</span>
    </div>
</template>


<script>
    export default{
        name:"TrendElement",
        props: ["trend"]
    }
</script>

<style scoped>
      .more-icon{
        font-size: 1.5rem;
        font-weight: bold;
    }

    .trend-box{
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
    }

    .trend-info{
        display: flex;
        flex-direction: column;
        margin-bottom: 1rem;
    }
</style>