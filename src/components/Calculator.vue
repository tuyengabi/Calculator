<template>
  <div class="calculator">
    <div class="screen">{{ output || 0 }}</div>
    <div class="btn" v-on:click="reset">C</div>
    <div class="btn" v-on:click="add('7')">7</div>
    <div class="btn" v-on:click="add('8')">8</div>
    <div class="btn" v-on:click="add('9')">9</div>
    <div class="btn operator">/</div>
    <div class="btn" v-on:click="del">del</div>
    <div class="btn" v-on:click="add('4')">4</div>
    <div class="btn" v-on:click="add('5')">5</div>
    <div class="btn" v-on:click="add('6')">6</div>
    <div class="btn operator">x</div>
    <div class="btn" v-on:click="percent">%</div>
    <div class="btn" v-on:click="add('1')">1</div>
    <div class="btn" v-on:click="add('2')">2</div>
    <div class="btn" v-on:click="add('3')">3</div>
    <div class="btn operator">-</div>
    <div class="btn">.</div>
    <div class="btn" v-on:click="add('0')">0</div>
    <div class="btn egal operator" v-on:click="result">=</div>
    <div class="btn operator">+</div>
  </div>
</template>

<script>
export default {
  name: 'Calculator',
  data() {
    return {
      output: '700',
    }
  },

  methods: {
    reset() {
      this.output = '';
    },

    del(output) {
      this.output = this.output.substring(0, this.output.length -1);
    },

    result(output) {
      this.output = eval(this.output);
    },

    percent() {
      this.output = this.output / 100;
    },

    add(operant) {
      this.output = this.output + operant;
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
