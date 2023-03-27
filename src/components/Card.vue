<script>
    export default {
        name: 'Card',
        props: {
            img: String,
            title: String,
            species: String
        }
    }
</script>

<template>
    <div class="ms_card mb-3 text-center">
        <div class="img"><img :src="img" alt=""></div>
        <h3 class="pt-5 pb-3 px-2 fw-semibold">{{ title }}</h3>
        <span>{{species}}</span>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/main.scss' as *;
@use '../assets/_partial/variables' as *;
.ms_card{
    height: 505px;
    width: 200px;
    background-color: $primary;
    img{
    width: 100%;
}
}
h3{
        font-size: 20px;
        color: $secondary;
        
    }

</style>