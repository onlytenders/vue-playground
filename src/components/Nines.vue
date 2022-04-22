<script>
export default {
    emits: ['message'],
    created() {
        this.$emit('message', 'some text from child')
    }
}
</script>