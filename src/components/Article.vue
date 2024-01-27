<template>
    <h2>{{ title }}</h2>
    <h2>Likes - {{ likes }}</h2>
    <h2>Comment: {{ comment }}</h2>
</template>

<script>
    export default {
        name: "Article",
        props: {
            title: {
                type: String,
                required: true
            },
            likes: Number,
            comment: {
                type: String,
                default: "Hello"
            }
        }
    }
</script>

<style scoped>

</style>