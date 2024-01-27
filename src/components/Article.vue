<template>
    <div>
        <h2>{{ title }}</h2>
        <h2 v-bind="$attrs">Likes - {{ likes }}</h2>
        <!-- Non Prop attributes like IdleDeadline, class etc get applied to the above h2 tag -->
        <h2>Comment: {{ comment }}</h2>
    </div>
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
    },
    inheritAttrs: false
    // id is applied by default on root component. 
}
</script>

<style scoped></style>