<template>
  <div class="keyboard">
    <Button>AC</Button>
    <Button>7</Button>
    <Button>8</Button>
    <Button>9</Button>
    <Button>/</Button>
    <Button>del</Button>
    <Button>4</Button>
    <Button>5</Button>
    <Button>6</Button>
    <Button>x</Button>
    <Button>%</Button>
    <Button>1</Button>
    <Button>2</Button>
    <Button>3</Button>
    <Button>-</Button>
    <Button>.</Button>
    <Button>0</Button>
    <Button>=</Button>
    <Button>+</Button>
  </div>
</template>

<script>
  import Button from './Button.vue';

  export default{
    name: 'Keyboard',
    components: {
      Button,
    },
  }
</script>

<style scoped>

</style>

