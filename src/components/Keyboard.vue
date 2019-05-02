<template>
  <div class="keyboard">
    <Button operator='AC'></Button>
    <Button operator='7' v-on:adding="btnAdd()"></Button>
    <Button operator='8'></Button>
    <Button operator='9'></Button>
    <Button operator='/'></Button>
    <Button operator='del'></Button>
    <Button operator='4'></Button>
    <Button operator='5'></Button>
    <Button operator='6'></Button>
    <Button operator='x'></Button>
    <Button operator='%'></Button>
    <Button operator='1'></Button>
    <Button operator='2'></Button>
    <Button operator='3'></Button>
    <Button operator='-'></Button>
    <Button operator='.'></Button>
    <Button operator='0'></Button>
    <Button operator='='></Button>
    <Button operator='+'></Button>
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

