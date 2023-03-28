<script>
import { store } from '../store';
import axios from 'axios';

export default {
    name: 'TypeSearch',
    data() {
        return {
            store,
            archetypes: []
        }
    },
    created() {
        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then((response) => {
                this.archetypes = response.data;
            })
    }
}
</script>

<template>
    <div class="container py-4">
        <select @change="$emit('search')" v-model="store.select" class="ms_select form-select bg-light"
            aria-label="Default select example">
            <option value="" selected>Open this select menu</option>
            <option> Alien </option>
            <option>-Eyes Dragon</option>
            <option>ABC</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/main.scss' as *;
@use '../assets/_partial/variables' as *;

.ms_select {
    width: 245px;
}
</style>