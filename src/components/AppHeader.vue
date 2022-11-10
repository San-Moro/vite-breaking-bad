<script>
export default {
    name: "AppHeader"
}
</script>

<template>
    <header class="d-flex pt-4">
        <img class="mx-3" src="../assets/img/Breaking_Bad_logo.svg.png" alt="logo">
        <h1>Breaking Bad Api</h1>
    </header>
</template>

<style lang="scss" scoped>
header {
    width: 100%;
    height: 100px;
    //DEBUG
    border: 1px solid white;

    img {
        height: 50px;
    }

    h1 {
        color: white;
    }
}
</style>