<script>
  export default {
    data() {
      return {
        cookies: true
      }
    },
    methods: {
      toggle() {
        this.cookies = !this.cookies
      }
    }
  }
</script>

<template>
  <h2 v-if="cookies">Cookies are allowed</h2>
  <h2 v-else>Cookies are not allowed</h2>
  <button @click="toggle" type="button" name="button" style="width: 100%;">toggle</button>
</template>
