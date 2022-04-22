<script>
export default {
    data () {
        return {
            text: ''
        }
    },

    watch: {
        text(text) {
            console.log(`the new text is ${text}`);
        }
    }
}
</script>

<template>
    <h3>Open the console</h3>
    <input type="text" v-model="text">
</template>