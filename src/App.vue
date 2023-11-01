<script setup>
  import Form from '@/components/Form.vue'
  import { ref, onMounted } from 'vue';



onMounted(() => {
  if (localStorage.theme === 'dark' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
    isDarkMode.value = true;
  } else {
    isDarkMode.value = false;
  }
})

  
</script>

<template>
  <div :class="isDarkMode ? 'dark' : ''">
    <div
      class="bg-blue-100 min-h-screen sm:p-10 p-5 flex flex-col justify-center dark:bg-[#0F172A] duration-500 transition-all ease-in-out">
      
      <h1 class="text-indigo-800 text-2xl font-bold text-center ">Formulario </h1>
      <Form />
      
    </div>
  </div>
</template>

<style  scoped>

</style>