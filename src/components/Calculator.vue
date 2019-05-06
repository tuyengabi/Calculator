<template>
  <div class="calculator">
    <div class="calculator__screen">{{ output || 0 }}</div>
    <div class="calculator__btn-reset" v-on:click="reset">C</div>
    <div class="calculator__btn" v-on:click="add('7')">7</div>
    <div class="calculator__btn" v-on:click="add('8')">8</div>
    <div class="calculator__btn" v-on:click="add('9')">9</div>
    <div class="calculator__btn-operator" v-on:click="add('/')">/</div>
    <div class="calculator__btn" v-on:click="add('4')">4</div>
    <div class="calculator__btn" v-on:click="add('5')">5</div>
    <div class="calculator__btn" v-on:click="add('6')">6</div>
    <div class="calculator__btn-operator" v-on:click="add('*')">x</div>
    <div class="calculator__btn--bg-grey" v-on:click="del">del</div>
    <div class="calculator__btn" v-on:click="add('1')">1</div>
    <div class="calculator__btn" v-on:click="add('2')">2</div>
    <div class="calculator__btn" v-on:click="add('3')">3</div>
    <div class="calculator__btn-operator" v-on:click="add('-')">-</div>
    <div class="calculator__btn--bg-grey calculator__btn--color-black" v-on:click="percent">%</div>
    <div class="calculator__btn--bg-grey calculator__btn--color-black" v-on:click="add('.')">.</div>
    <div class="calculator__btn" v-on:click="add('0')">0</div>
    <div class="calculator__btn-operator" v-on:click="result">=</div>
    <div class="calculator__btn-operator" v-on:click="add('+')">+</div>
  </div>
</template>

<script>
export default {
  name: 'Calculator',
  data() {
    return {
      output: '0',
    }
  },

  methods: {
    reset() {
      this.output = '';
    },

    del() {
      this.output = this.output.substring(0, this.output.length -1);
    },

    result() {
      this.output = eval(this.output);
    },

    percent() {
      this.output = this.output / 100;
    },

    add(operant) {
      this.ouput= '';
      this.output = this.output + operant;
    }
  }
}
</script>

<style scoped lang="scss">
.calculator {
  width: 50%;
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-rows: minmax(8%, auto);
  font-size: 4rem;
}

.calculator__screen {
  height: 10rem;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 6rem;
  grid-column: 1 / 6;
  color: white;
  background-color: rgba(0, 0, 0, 0.8);
}

.calculator__btn {
  color: black;
  background-color: rgba(0, 0, 0, 0.2);
  border: 1px solid black;
}

.calculator__btn--bg-grey {
  color: white;
  background-color: rgba(0, 0, 0, 0.4);
  border: 1px solid black;
}

.calculator__btn--color-black {
  color: black;
  border: 1px solid black;
}

.calculator__btn-reset {
  grid-row: 2 / 4;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  background-color: rgba(0, 0, 0, 0.6);
  border: 1px solid black;
}

.calculator__btn-operator {
  background-color: rgba(255, 215, 10, 0.4);
  color: black;
  border: 1px solid black;
}
</style>
