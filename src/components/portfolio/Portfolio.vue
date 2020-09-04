<template>
    <div>
        <app-stock v-for="stock in stocks" :stock="stock" v-bind:key="stock.id"></app-stock>
    </div>
</template>

<style scoped>
    .danger {
        border: 1px solid red;
    }
</style>

<script>
    import {mapGetters} from 'vuex';
    import Stock from "./Stock.vue";
    export default {
        
        computed: {
          ...mapGetters({
              stocks: 'stockPortfolio'
          }) 
        },
        components: {
            appStock: Stock
        }
        
    }
</script>