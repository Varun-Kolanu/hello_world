<template>
    <div>
        <h2>Component B: {{ username }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'CompB',
        inject: ['username']
    }
</script>

<style scoped>

</style>