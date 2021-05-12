<template>
  <div class="home">
    <Jokes v-bind:jokeList="jokeList" />
    <button @click="fetchJokes" class="btn btn-success btn-lg">Fetch More!</button>
  </div>
</template>

<script>
// @ is an alias to /src
import axios from 'axios';
import Jokes from '@/components/Jokes.vue';

export default {
  name: "Home",
  data() {
    return {
      jokeList: []
    }
  },
  components: {
    Jokes,
  },
  created(){
    axios.get("https://official-joke-api.appspot.com/jokes/programming/ten")
      .then(res => this.jokeList = res.data)
  },
  methods: {
    fetchJokes: function(){
      axios.get("https://official-joke-api.appspot.com/jokes/programming/ten")
        .then(res => this.jokeList = res.data)
    }
  }
}


</script>

<style lang="scss" scoped>
  .home{
    margin: 2vh 3vw;

    button{
      display: block;
      margin: 5vh auto;
      font-size: 1.5rem;
      font-weight: bold;
    }
  }
</style>