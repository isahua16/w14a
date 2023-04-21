<template>
    <div>
        <button @click="send_snake_joke">Snake Joke</button>
    </div>
</template>

<script>
    export default {
        mounted () {
            //Listen for the receive_joke event, replace all spaces within the string and store it into a variable
            this.$root.$on(`receive_joke`, joke => this.joke = joke.replaceAll(` `, `_`));
        },
        data() {
            return {
                snake_joke: undefined
            }
        },
        methods: {
            send_snake_joke: function() {
                //Emit this joke on click
                this.$root.$emit(`receive_snake_joke`, this.joke);
            }
        }
    }
</script>

<style scoped>

</style>