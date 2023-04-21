<template>
    <div>
        <button @click="send_normal_joke">Normal Joke</button>
    </div>
</template>

<script>
    export default {
        mounted () {
            this.$root.$on(`receive_joke`, joke => this.joke = joke);
        },
        data() {
            return {
                normal_joke: undefined
            }
        },
        methods: {
            send_normal_joke: function() {
                this.$root.$emit(`receive_normal_joke`, this.joke);
            }
        }
    }
</script>

<style scoped>

</style>