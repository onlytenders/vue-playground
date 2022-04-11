<script>
export default {
  data() {
    return {
      text: ''
    }
  },
  methods: {
    onType(e) {
      this.text = e.target.value
    }
  }
}
</script>

<template>
<input type="text" name="" value="" placeholder="type something" @input="onType">
<p>{{ text }}</p>  
</template>
