<template>
    <div>
        <h1>Trade or View your Porfolio</h1>
        <hr>
        <p>Your fund: {{funds | currency}}</p>
    </div>
</template>
<script>
export default {
    computed: {
        funds() {
            return this.$store.getters.funds;
        }
    }
}
</script>