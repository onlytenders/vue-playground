<script>
  export default {
    data() {
      return {
        counter: 0
      }
    }
  }
</script>

<template>
  <button @click="counter++" type="button" name="button">The score is: {{ counter }}</button>
</template>
