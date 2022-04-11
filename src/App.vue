<script>
import First from './components/First.vue'
import Second from './components/Second.vue'

export default {
  components: {
    First,
    Second
  }
}
</script>

<template>

<div style="display:flex;">
  <div class="">
    <First />
  </div>
  <div class="">
    <Second />
  </div>
</div>

</template>
