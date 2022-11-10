<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import CharactersGrid from './components/CharactersGrid.vue';
import {store} from "./store";

export default {
  components: {
    AppHeader,
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
    })
  }
}
</script>

<template>
  <AppHeader />
  <main>
    <div class="ms_container p-5">
      <CharactersGrid />

    </div>
  </main>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;

</style>