<template>
  <div class="calculator">
    <div class="screen">0</div>
    <div class="btn">C</div>
    <div class="btn">7</div>
    <div class="btn">8</div>
    <div class="btn">9</div>
    <div class="btn operator">/</div>
    <div class="btn">del</div>
    <div class="btn">4</div>
    <div class="btn">5</div>
    <div class="btn">6</div>
    <div class="btn operator">x</div>
    <div class="btn">%</div>
    <div class="btn">1</div>
    <div class="btn">2</div>
    <div class="btn">3</div>
    <div class="btn operator">-</div>
    <div class="btn">.</div>
    <div class="btn">0</div>
    <div class="btn egal operator">=</div>
    <div class="btn operator">+</div>
  </div>
</template>

<script>
export default {
  name: 'Calculator',
  data() {
    return {
      output: '',
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.calculator {
  margin: auto;
  padding: auto;
  width: 50%;
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-rows: minmax(8%, auto);
  font-size: 4rem;
}

.screen {
  grid-column: 1 / 6;
  color: white;
  background-color: rgba(0, 0, 0, 0.8);
}

.egal {
  grid-column: 3 / 5;
}

.btn {
  color: white;
  background-color: rgba(0, 0, 0, 0.4);
  border: 1px solid black;
}

.operator {
  background-color: rgba(255, 215, 10, 0.4);
  color: black;
}
</style>
