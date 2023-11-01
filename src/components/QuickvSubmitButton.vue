<script setup>
  
</script>

<template>
  <button data-qv-submit  class="m-1 px-4 py-2 border-2 border-blue-600 rounded-full hover:bg-blue-600 hover:text-white hover:transition-all hover:duration-300 dark:text-white">
    <slot></slot>
  </button>
</template>

<style  scoped>
[data-qv-submit]:disabled {
  background:#ccc
}




</style>