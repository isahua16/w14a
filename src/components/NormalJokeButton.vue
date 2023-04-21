<template>
    <div>
        <button @click="send_normal_joke">Normal Joke</button>
    </div>
</template>

<script>
    export default {
        mounted () {
            ////Listen for the receive_joke event and store it into a variable
            this.$root.$on(`receive_joke`, joke => this.joke = joke);
        },
        data() {
            return {
                normal_joke: undefined
            }
        },
        methods: {
            send_normal_joke: function() {
                //emit normal joke on click
                this.$root.$emit(`receive_normal_joke`, this.joke);
            }
        }
    }
</script>

<style scoped>

</style>