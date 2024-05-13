<template>
  <aside class="sidebar-panel">
    <h1 style="color:#E57D70"><strong><em>CRM.io</em></strong></h1>
    <NavItem title="Dashboard" icon="ic:outline-dashboard" />
    <section class="nav-list-container">
      <h3>Management</h3>
      <NavItem icon="ic:outline-file-copy" title="Document" />
      <NavItem icon="ri:contacts-book-upload-line" title="Contact" />
      <NavItem icon="fluent:projection-screen-16-regular" title="Prospect" />
      <NavItem icon="carbon:workflow-automation" title="Workflow" />
    </section>
    <section class="nav-list-container">
      <h3>Connection</h3>
      <NavItem icon="mdi:chat-outline" title="Chat" />
      <NavItem icon="ph:briefcase" title="Marketing" />
      <NavItem icon="ic:outline-email" title="Email" />

    </section>
    <section class="nav-list-container">
      <h3>Customer</h3>
      <NavItem icon="grommet-icons:transaction" title="Transaction" />
      <NavItem icon="mdi:gear" title="Maintenance" />
    </section>
  </aside>
</template>

<script setup lang="ts">
import NavItem from './NavItem.vue'
import { Icon } from '@iconify/vue'
</script>

<style scoped>
.sidebar-panel {
  display: none;
}

.nav-list-container {
  color: #28436B;
  border-bottom: 1px solid #28436B;
  padding: 0.75rem;
}

@media (min-width: 1024px) {
  .sidebar-panel {
    display: flex;
    min-width: 15vw;
    color: white;
    padding: 1rem 1.5rem;
    background-color: #031737;
    height: 95dvh;
    flex-direction: column;
    row-gap: 1.5rem;
  }
}
</style>