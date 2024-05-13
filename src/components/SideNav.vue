<template>
  <aside class="sidebar-panel">
    <h1 style="color:#E57D70"><strong>CRM.io</strong></h1>
  </aside>
</template>

<script setup lang="ts">

</script>

<style scoped>
.sidebar-panel {
  display: none;
}

@media (min-width: 1024px) {
  .sidebar-panel {
    display: block;
    min-width: 12vw;
    color: white;
    padding: 1rem 1.5rem;
    background-color: #031737;
    height: 95dvh;
  }
}
</style>