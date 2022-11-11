<script>
export default {
    name: "CharacterCard",
    props: {
        character: Object
    }
}
</script>

<template>
    <div class="card-item text-center mb-4 pb-2">
        <img class="p-3" :src="character.img" alt="">
        <h3>{{ character.name }}</h3>
        <p class="pt-2">{{ character.category }} <br> {{ character.status }}</p>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
.card-item {
    height: 450px;
    background-color: $main-bg-color;

    h3 {
        color: white;
        font-size: 16px;
        text-transform: uppercase;
    }

    p {
        color: $subtext-color;
        font-size: 18px;
    }
}

</style>
