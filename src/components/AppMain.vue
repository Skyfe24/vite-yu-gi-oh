<script>
import { store } from '../store.js';

export default {
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <!-- main-->

    <main>
        <h2>POKèMON</h2>
        <div v-for="pokemon in store.pokeList.docs">
            <img :src="pokemon.imageUrl">
            <h2>{{ pokemon.name }}</h2>
            <h5>{{ pokemon.type1 }}</h5>
            <h5>{{ pokemon.type2 }}</h5>
        </div>

    </main>
    <h2>LOAD MORE</h2>
    <section></section>
</template>


<style scoped>
main {
    background-color: rgb(245, 80, 30);
    min-height: 500px;
}

section {
    background-color: rgb(59, 135, 250);
    min-height: 200px;
}

h2 {
    background-color: rgb(59, 135, 250);
    display: inline-block;
    color: white;
    padding: 8px;
    padding-right: 30px;
    padding-left: 30px;
}

h5 {
    background-color: rgb(4, 80, 8);
    display: inline-block;
    color: white;
    padding: 8px;
    padding-right: 30px;
    padding-left: 30px;
}

img {
    width: 200px;
    height: 200px;
}
</style>