<template>
  <div>
    <SearchJokes v-on:search-text="searchText" />
    <Joke
      v-for="joke in jokes"
      v-bind:key="joke.id"
      v-bind:id="joke.id"
      v-bind:joke="joke.joke"
    />
  </div>
</template>

<script>
import axios from 'axios';
import Joke from '~/components/Joke';
import SearchJokes from '~/components/SearchJokes';

export default {
  components: {
    Joke,
    SearchJokes,
  },
  data() {
    return {
      jokes: []
    }
  },
  async created() {
    const config = {
      headers: {
        Accept: 'application/json'
      }
    };
    try {
      const res = await axios.get(`https://icanhazdadjoke.com/search`, config);
      this.jokes = res.data.results; // spremi u jokes array definiran u data()
    }
    catch (err) {
      console.log(err);
    }
  },
  methods: {
    async searchText(emittedText) {
      const config = {
        headers: {
          Accept: 'application/json'
        }
      };
      try {
        const res = await axios.get(`https://icanhazdadjoke.com/search?term=${emittedText}`, config);
        this.jokes = res.data.results;
      }
      catch (err) {
        console.log(err);
      }
    }
  },
  head() {
    return {
      title: 'Jokes page',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for corny dad jokes',
        }
      ]
    }
  }
}
</script>

<style>

</style>