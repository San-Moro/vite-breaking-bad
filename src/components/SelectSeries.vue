<script>
import {store} from "../store";
export default {
    name: "SelectSeries",
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <div class="select-series py-3 mb-2">
        <select class="form-select" 
            aria-label="Default select example" 
            v-model="store.selectForm"
            @change="$emit('select')">
            <option selected>Select Category</option>
            <option value="1">Breaking Bad</option>
            <option value="2">Better Call Saul</option>
        </select>
    </div>

</template>

<style lang="scss" scoped>
.select-series {
    width: 70%;

    .form-select {
        width: 30%;
    }
}
</style>