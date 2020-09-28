<template>
    <div id="tweets-container">
        <h1>Tweets</h1>
    <button id="display-change" @click="grid =! grid"> Change Display </button>
<div id="grid" :class=" { grid: grid}">
    <div id="tweet-container" v-for="tweet in tweets" v-bind:key="tweet">
        <h3> {{ tweet.content }} </h3>
    <p> {{ " Posted By: " + tweet.name }} </p>
    <p> {{ "Created On: " + tweet.date }} </p>

    </div>
</div>
    </div>
</template>

<script>
    export default {
        name: "tweets-view",
        data: function (){
            return {
                tweets: [
                    {
                        content: "Hello World!",
                        name: "Sie",
                        date: "09-01-2020"
                    },
                    {
                        content: "What? I am confusion",
                        name: "Mylee",
                        date: "08-01-2020"
                    },
                     {
                        content: "Why are you the way you are?",
                        name: "Ben",
                        date: "09-15-2020"
                    },
                     {
                        content: "I love french fries!!!!",
                        name: "Lucas",
                        date: "09-22-2020"
                    },
                     {
                        content: "Love all you want, be who you want, and express yourself how ever feels best.",
                        name: "Andrea",
                        date: "09-01-2020"
                    },
                     {
                        content: "It is 2020.. why have you all not accepted that BLM?? Who RAISED you?!",
                        name: "Andi",
                        date: "09-13-2020"
                    }
                ],
                grid:true,
            }
        },
    }
</script>

<style scoped>
.grid {
    display: grid;
    justify-items: center;
    align-items: center;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    }
    button {
        width: 10%;
        
    }


</style>