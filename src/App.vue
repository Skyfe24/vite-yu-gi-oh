<script>
import axios from 'axios';
import AppMain from './components/AppMain.vue';
import pokeList from './store';


export default {
  data() {
    return {
      pokeList []
    }
  },
  components: {
    AppMain, ComicCard
  }
  created() {
    axios.get(endpoint).then(res => {
      store.pokeList = res.data.results;
    })
  }

}

</script>

<template>
  <!-- header-->
  <AppHeader />
  <AppHero />

  <!-- main-->
  <AppMain />
</template>


<style>
h3 {
  color: rgb(231, 65, 23)
}
</style>