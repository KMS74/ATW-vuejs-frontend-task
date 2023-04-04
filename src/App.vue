<template>
  <TheNavbar />
  <div class="main-container">
    <RouterView />
  </div>
</template>

<script>
import TheNavbar from './components/TheNavbar.vue'

export default { components: { TheNavbar } }
</script>

<style scoped></style>
