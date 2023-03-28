<script>
import Card from './Card.vue';
import { store } from '../store';

export default {
    name: 'CardList',
    components: {
        Card
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="container ms_container">
        <div class="row mb-2">
            <div class="col-6 col-sm-2" v-for="card in store.cards.slice(0,50)">
                <Card 
                :img="card.card_images[0].image_url"
                :title="card.name"
                :species="card.archetype"
                 ></Card>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/_partial/variables' as *;
.ms_container{
    background-color: $secondary;
    padding: 30px;
}
</style>