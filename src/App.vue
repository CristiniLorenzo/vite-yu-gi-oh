<script>
import axios from 'axios';
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppSearch from './components/AppSearch.vue';



export default {
  components: {
    AppHeader,
    AppMain,
    AppSearch,

  },
  data() {
    return {
      store
    };
  },
  methods: {
    getCardsFromApi() {
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
      .then((response) => {
        // console.log(response.data);
        store.cards = response.data.data
      })
    },
    getArchetypeFromApi() {
      axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
      .then((response) => {
        console.log(response.data);
        store.archetypes = response.data;
      })
    }
  },
  mounted() {
    this.getCardsFromApi();
    this.getArchetypeFromApi()
  }
}
</script>

<template>
<header>
  <AppHeader></AppHeader>
</header>
<main>
  <AppSearch></AppSearch>
  <AppMain></AppMain>
</main>
  
</template>

<style lang="scss">
@use './style/generics.scss'

</style>