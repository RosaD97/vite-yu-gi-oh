<script>
import TypeSearch from './TypeSearch.vue';
import CardList from './CardList.vue';
export default {
    name: 'AppMain',
    components: {
        TypeSearch,
        CardList
    }
}
</script>

<template>
    <main>
        <TypeSearch></TypeSearch>
        <CardList></CardList>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/_partial/variables' as *;
main{
    background-color: $primary;

}
</style>