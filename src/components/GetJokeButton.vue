<template>
    <div>
        <button @click="fetch_joke">Get a joke</button>
        <h4>{{ error_message }}</h4>
    </div>
</template>

<script>
import axios from 'axios';
    export default {
        methods: {
            fetch_joke: function() {
                axios.request({
                    url: `https://ron-swanson-quotes.herokuapp.com/v2/quotes`
                }).then((res) => {
                    let joke = res.data[0];
                    this.$root.$emit(`receive_joke`, joke);
                }).catch(() => {
                    this.error_message = `Something went wrong... try again.`
                });
            }
        },
        data() {
            return {
                error_message: undefined
            }
        },
    }
</script>

<style scoped>

</style>