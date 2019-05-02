<template>
  <div class="button" v-on:click="$emit('adding')">
      {{ operator }}
  </div>
</template>

<script>
  export default{
   name: 'Button',
   props: {
      operator: String
    }
  }
  
</script>

<style scoped>

</style>

