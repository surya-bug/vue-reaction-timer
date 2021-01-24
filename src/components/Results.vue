<template>
  
  <p> ReactionTime : {{score}} ms </p>

  <p class="rank"> {{ rank }} </p>
</template>

<script>
export default {
props: ['score'],

data(){

    return {

        rank:null,


    }
},

mounted(){

    if(this.score  < 250){

        this.rank = "Ninja speeed "

    }else if(this.score < 400 ){

        this.rank = "You are a quickie!"
    }else{
        this.rank = "As slow as a snail !"
    }


    }
}



</script>

<style>

.rank {

    font-size: 1.4em;
    color: crimson;
    font-weight: bold;
}

</style>
