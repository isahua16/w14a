<template>
    <div>
        <h3>{{ joke }}</h3>
    </div>
</template>

<script>
    export default {
        mounted () {
            //Listen for all three display buttons and store it's answer into the joke variable. Each time you reclick, the variable gets updated and displayed in the template HTML.
            this.$root.$on(`receive_normal_joke`, joke => this.joke = joke);
            this.$root.$on(`receive_loud_joke`, joke => this.joke = joke);
            this.$root.$on(`receive_snake_joke`, joke => this.joke = joke);
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