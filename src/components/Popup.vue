<template>
    <div>
        <h2>This is Popup</h2>
        <button @click="$emit('close', 'Varun')">Close</button>
        <!-- second parameter is name -->
    </div>
</template>

<script>
    export default {
        name: 'Popup',
        emits: ['close']
    }
</script>

<style scoped>

</style>