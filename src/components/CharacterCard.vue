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
@use "../styles/partials/variables";
.card-item {
    height: 450px;
    background-color: #2e3a46;

    h3 {
        color: white;
        font-size: 16px;
        text-transform: uppercase;
    }

    p {
        color: #62666a;
        font-size: 18px;
    }
}

</style>
