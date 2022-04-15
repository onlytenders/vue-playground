<script>
import First from './components/First.vue'
import Second from './components/Second.vue'
import Third from './components/Third.vue'
import Fourth from './components/Fourth.vue'
import Fifth from './components/Fifth.vue'

export default {
  components: {
    First,
    Second,
    Third,
    Fourth,
    Fifth
  }
}
</script>

<template>

<div class="container">
  <div class="item">
    <First />
  </div>
  <div class="item">
    <Second />
  </div>
  <div class="item">
    <Third />
  </div>
  <div class="item">
    <Fourth />
  </div>
  <div class="item">
    <Fifth />
  </div>
</div>

</template>

<style media="screen">
  .container {
    display: flex;
    width: 100%;
    justify-content: space-around;
  }

  .item {
    border: 2px solid black;
    padding: 15px;
  }
</style>
