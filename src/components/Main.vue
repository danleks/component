<template>
    <div>

        <app-header></app-header>
        <div class="container">
        <app-colors></app-colors>
    </div>
    </div>


</template>

<script>
import Header from './Header.vue';
import Colors from './Colors.vue';


export default {
    components: {
        'app-header': Header,
        'app-colors': Colors
    }
}
</script>


<style>

</style>
