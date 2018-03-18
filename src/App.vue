<template>
    <div class="container">
        <div class="div">
            <ul>
                <li v-for="quote in quotes" :key="quote.id">{{ quote }}</li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                quotes: [ "I'm a Potato ! :3", "Hello, me too ! :)" ],
                maxQuotes: 10
            }
        }
    }
</script>

<style>
</style>
