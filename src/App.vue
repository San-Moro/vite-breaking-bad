<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import SelectSeries from './components/SelectSeries.vue';
import {store} from "./store";
import CharactersGrid from './components/CharactersGrid.vue';

export default {
  components: {
    AppHeader,
    SelectSeries,
    CharactersGrid
  },
  data() {
    return {
      store
    }
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.store.characters = resp.data;
      console.log(this.store.characters);
    });
  },
  methods: {
    filterSerie() {
      axios.get(`https://www.breakingbadapi.com/api/characters?category=${this.store.selectForm}`).then((resp) => {
      this.store.characters = resp.data;
    })
  }
}

</script>

<template>
  <AppHeader />
  <main>
    <div class="ms_container">
      <SelectSeries @select="filterSerie" />
      <CharactersGrid />

    </div>
  </main>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;

</style>