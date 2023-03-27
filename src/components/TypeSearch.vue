<script>
export default {
    name: 'TypeSearch'
}
</script>

<template>
    <div class="container-fluid">
        <select class="ms_select form-select bg-light" aria-label="Default select example">
            <option selected>Open this select menu</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
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