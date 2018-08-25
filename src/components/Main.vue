<template>
    <div class="container">
        <app-header></app-header>
        <app-colors></app-colors>
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
