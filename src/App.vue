<script>
export default {
  data() {
    return {
      message: 'hello world',
      classTitle: 'titleBlue'
    }
  },
  methods: {
    reverseString() {
      this.message = this.message.split('').reverse().join('')
    },

    changeColor() {
      if (this.classTitle == 'titleBlue') {
        this.classTitle = 'titleRed'
      } else {
        this.classTitle = 'titleBlue'
      }
    }
  }
}
</script>

<template>
<h1 :class="classTitle">{{ message }}</h1>
<button @click="reverseString">reverse</button>
<button @click="changeColor">color</button>
</template>

<style>
.titleBlue {
  color: blue;
}

.titleRed {
  color: red;
}
</style>
