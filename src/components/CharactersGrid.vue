<script>
import {store} from "../store";
import CharacterCard from "./CharacterCard.vue";

export default {
    name: "CharactersGrid",
    components: {
        CharacterCard
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="row row-cols-5">
        <div class="col">
            <CharacterCard />
        </div>
        <div class="col">
            <CharacterCard />
        </div>
        <div class="col">
            <CharacterCard />
        </div>
        <div class="col">
            <CharacterCard />
        </div>
        <div class="col">
            <CharacterCard />
        </div>
        <div class="col">
            <CharacterCard />
        </div>
    </div>
</template>

<style lang="scss" scoped></style>