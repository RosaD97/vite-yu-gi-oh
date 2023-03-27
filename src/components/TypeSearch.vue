<script>

export default {
    name: 'TypeSearch'
}
</script>

<template>
    <div class="container py-4">
        <select class="ms_select form-select bg-light" aria-label="Default select example">
            <option selected>Open this select menu</option>
            <option value="1">Alien</option>
            <option value="2">Alien</option>
            <option value="3">Alien</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/main.scss' as *;
@use '../assets/_partial/variables' as *;
.ms_select{
    width: 245px;
}
</style>