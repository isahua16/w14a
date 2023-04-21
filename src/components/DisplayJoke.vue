<template>
    <div>
        <h3>{{ joke }}</h3>
    </div>
</template>

<script>
    export default {
        mounted () {
            this.$root.$on(`receive_joke`, joke => this.joke = joke);
        },
        data() {
            return {
                joke: undefined
            }
        },
    }
</script>

<style scoped>

</style>