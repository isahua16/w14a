<template>
    <div>
        <button @click="send_snake_joke">Snake Joke</button>
    </div>
</template>

<script>
    export default {
        mounted () {
            this.$root.$on(`receive_joke`, joke => this.joke = joke.replaceAll(` `, `_`));
        },
        data() {
            return {
                snake_joke: undefined
            }
        },
        methods: {
            send_snake_joke: function() {
                this.$root.$emit(`receive_snake_joke`, this.joke);
            }
        }
    }
</script>

<style scoped>

</style>