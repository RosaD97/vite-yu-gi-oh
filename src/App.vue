<script>
import axios from 'axios';
import { store } from './store';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain
  },
  data() {
    return {
      store
    }
  },
  methods: {
    search(){
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
        params: {
          archetype: store.select
        }
      })
      .then((response) => {
        this.store.cards = response.data.data;
        this.store.cardsFounds = response.data.data.length;
      })
    }
  },
  created() {
    this.search();
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
</template>

<style></style>
