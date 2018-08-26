<template>
   <div class="row mb-4">
        <div class="col-md-6">
            <ul class="list-group">
                <app-color v-for="color in colors" :key="color.id" :color="color"></app-color>
            </ul>
       </div>
       <div class="col-md-6">

                <app-color-info></app-color-info>

       </div>
   </div>
</template>

<script>

    import Color from './Color.vue';
    import ColorInfo from './ColorInfo.vue';

    export default {
        data: function() {
            return {
                colors: [
                        {id: 1, color: 'Peter river', hex: '#3498db'},
                        {id: 2, color: 'Orange hibiscus', hex: '#fd9644'},
                        {id: 3, color: 'Maximum blue green', hex: '#2bcbba'},
                        {id: 4, color: 'Fusion red', hex: '#fc5c65'}
                    ]
            }
        },

        components: {
            'app-color': Color,
            'app-color-info': ColorInfo
        }
    }
</script>


<style>

</style>
