<template>
  <p>Reaction time: {{ score }} ms</p>
  <p class="rank">Rank: {{ rank }}</p>
</template>

<script>
export default {
    props: ["score"],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        console.log("Mounted")
        if(this.score < 250) {
            this.rank = "Flash"
        } else if (this.score < 480) {
            this.rank = "Average Human Being"
        } else {
            this.rank = "Tortoise"
        }
        console.log(this.rank)
    }
}
</script>

<style>
.rank {
    font-size: 1.4em;
    color : rgb(19, 153, 206);
    font-weight : bold; 
}

</style>