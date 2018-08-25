<template>

    <li class="list-group-item list-group-item-action" @click="showColor()">Color: {{ color.color }}</li>

</template>

<script>

import { EventBus } from '../main.js';

export default {

    props: {
        color: {
            type: Object,
            required: true
        }
    },

    methods: {
        showColor() {
            EventBus.$emit('show-color', this.color);
        }
    }
}
</script>


<style lang="scss" scoped>
    .list-group {

        &-item {
            cursor: pointer;
        }
    }
</style>