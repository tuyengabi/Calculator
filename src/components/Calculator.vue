<template>
  <div>
    <Screen></Screen>
    <Keyboard></Keyboard>
  </div>
</template>

<script>
  import Screen from './Screen.vue';
  import Keyboard from './Keyboard.vue';

  export default{
    name: 'Calculator',
    components: {
      Screen,
      Keyboard,
    }
    data: function() {
      return {
        newInput;
        oldInput
      }

    }
    props: [],

    methods: {
      btnadd: function() {
       this.newInput = this.oldInput + this.operator 
      },

      btnreset: function() {
        this.newInput = 0
      },

      btndel: function() {
        this.newInput = oldInput.substring(0, oldInput -1)
      },

      btnresult: function() {
        Number(this.newInput)
      }
    }
    
  }
</script>

<style scoped>

</style>

