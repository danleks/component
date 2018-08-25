<template>
        <div v-if="!this.lColor" class="color-init-block">
            <p class="color-init-block__text">Choose color</p>
        </div>
        <div v-else class="color-info-block" v-bind:style="{'background-color': lColor}">
            <p class="color-info-block__text">Hex code: {{ lColor }}</p>
            <button class="btn btn-outline-light text-dark btn-sm color-info-block__button" @click="resetColor">Reset Color</button>
        </div>
</template>

<script>

import { EventBus } from '../main.js';

export default {

    data: function() {
        return {
            lColor: null,
            message: 'Color is not chosen yet.'
        }
    },

    created() {
        EventBus.$on('show-color', (color) => {
            this.lColor = color.hex;
        })
    },

    methods: {
        resetColor() {
            this.lColor = null;
        }
    }

}

</script>


<style scoped lang="scss">
    .color-init-block {
        height: 100%;
        background-color: rgba(#ccc, .4);

        &__text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);

            font-size: 24px;
            text-transform: uppercase;
            color: #000;
        }
    }
    .color-info-block {
        position: relative;
        height: 100%;
        border-radius: 2px;


        &__text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);

            font-size: 24px;
            text-transform: uppercase;
            color: #fff;
        }

        &__button {
            position: absolute;
            top: 70%;
            left: 50%;
            transform: translate(-50%, 0%);
        }

    }
</style>