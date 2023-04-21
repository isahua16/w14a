<template>
    <div>
        <button @click="send_loud_joke">Loud Joke</button>
    </div>
</template>

<script>
    export default {
    mounted () {
        //Listen for the receive_joke event, make the content all caps and store it into a variable
        this.$root.$on(`receive_joke`, joke => this.joke = joke.toUpperCase());
    },
    data() {
        return {
            joke: undefined
        }
    },
    methods: {
        send_loud_joke: function() {
            //Emit the joke on click.
            this.$root.$emit(`receive_loud_joke`, this.joke);
        }
    }
        }
</script>

<style scoped>

</style>