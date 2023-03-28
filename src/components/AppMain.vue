<script>
import TypeSearch from './TypeSearch.vue';
import CardList from './CardList.vue';
import { store } from '../store';
export default {
    data() {
        return {
            store
        }
    },
    name: 'AppMain',
    components: {
        TypeSearch,
        CardList
    }
}
</script>

<template>
    <main>
        <TypeSearch @search="searchArchetype"></TypeSearch>
        <div>trovate {{ store.cardsFounds }} carte</div>
        <CardList></CardList>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/_partial/variables' as *;

main {
    background-color: $primary;

}
</style>