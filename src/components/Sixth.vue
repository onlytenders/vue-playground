<script>
export default {
    mounted() {
        this.$refs.textbox.textContent = "another"
    }
}
</script>

<template>

<p ref="textbox">something</p>

</template>
