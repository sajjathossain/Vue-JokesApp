<template>
    <div>
        <div v-if="jokeList.length === 0" class="container">
            <h1 class="text-warning">No Jokes Found!</h1>
        </div>

        <div v-if="jokeList.length > 0" class="container-fluid">
            <div class="row">
                <div v-for="joke in jokeList" v-bind:key="joke.id" >
                    <div class="col-md-3 mt-3">
                        <div class="card">
                            <div class="card-body">
                                <h3 class="card-title">Joke {{jokeList.indexOf(joke) +1}}</h3>
                                <b class="card-text">{{joke.setup}}</b>
                                <p><b>Ans : </b>{{joke.punchline}}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Jokes',
    props: ["jokeList"],
}
</script>

<style lang="scss" scoped>
    .row{
        display: flex;
        justify-content: center;
    
        .card {
            height: 20vh;
            width: 20vw;
            border-radius: 1rem;
            transition: ease-in-out 0.333s all;
            
            &:hover{
                cursor: pointer;
                transform: scale(1.05);
                box-shadow: 5px 5px 5px 3px #ccc;
            }
        }
    }

</style>