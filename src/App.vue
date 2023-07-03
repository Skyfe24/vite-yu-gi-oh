<script>
import axios from 'axios';
import AppMain from './components/AppMain.vue';
import { store } from './store';


export default {
  data() {
    return {

    }
  },
  components: {
    AppMain,
  },
  created() {
    axios.get("https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons").then(res => {
      store.pokeList = res.data;
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