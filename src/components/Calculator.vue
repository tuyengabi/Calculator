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
  }
</script>

<style scoped>

</style>

