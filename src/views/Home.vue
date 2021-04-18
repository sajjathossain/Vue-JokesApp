<template>
  <div class="home">
    <Jokes v-bind:jokeList="jokeList" />
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
    }
}


</script>

<style lang="scss" scoped>
  .home{
    margin: 2vh 3vw;
  }
</style>