<template>
    <div>
        <button @click="send_loud_joke">Loud Joke</button>
    </div>
</template>

<script>
    export default {
    mounted () {
        this.$root.$on(`receive_joke`, joke => this.joke = joke.toUpperCase());
    },
    data() {
        return {
            joke: undefined
        }
    },
    methods: {
        send_loud_joke: function() {
            this.$root.$emit(`receive_loud_joke`, this.joke);
        }
    }
        }
</script>

<style scoped>

</style>