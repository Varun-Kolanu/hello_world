<template>
    <div>
        <h2>This is Popup</h2>
        <input type="text" v-model="name"/>
        <button @click="$emit('close', name)">Close</button>
        <!-- second parameter is name -->
    </div>
</template>

<script>
    export default {
        name: 'Popup-Component',
        data() {
            return {
                name: ''
            }
        },
        emits: {
            close: (name) => {
                if (!name) return false;
                return true;
            }
        }
    }
</script>

<style scoped>

</style>