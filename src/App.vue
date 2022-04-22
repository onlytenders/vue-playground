<script>
import First from './components/First.vue'
import Second from './components/Second.vue'
import Third from './components/Third.vue'
import Fourth from './components/Fourth.vue'
import Fifth from './components/Fifth.vue'
import Sixth from './components/Sixth.vue'
import Seventh from './components/Seventh.vue'
import Eights from './components/Eights.vue'
import Nines from './components/Nines.vue'

export default {
  components: {
    First,
    Second,
    Third,
    Fourth,
    Fifth,
    Sixth,
    Seventh,
    Eights,
    Nines
  },
  
  data() {
    return {
      emmitedText: 'no text yet'
    }
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

<div class="container">
  <div class="item">
    <Sixth />
  </div>
  <div class="item">
    <Seventh />
  </div>
  <div class="item">
    <Eights sometext="not okay"/>
  </div>
  <div class="item">
    <Nines @message="(msg) => emmitedText = msg" />
    <h3>{{ emmitedText }}</h3>
  </div>
</div>

</template>

<style media="screen">

  .container {
    display: flex;
    width: 100%;
    justify-content: space-around;
    margin-top: 50px;
  }

  .item {
    border: 2px solid black;
    padding: 15px;
  }
</style>
