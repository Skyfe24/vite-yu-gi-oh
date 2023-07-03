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
        <span> {{ store.pokeList }}</span>

    </main>
    <h2>LOAD MORE</h2>
    <section></section>
</template>


<style scoped>
main {
    background-color: rgb(53, 63, 63);
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
</style>