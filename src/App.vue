<template>
  <div class="app-container">
    <SideNav />
    <main class="mid-panel">
      <nav class="nav-container">
        <h1>Overview</h1>
        <div>
        </div>
        <div style="display: flex; column-gap: 0.25rem; align-items: center; ">
          <Icon icon="mdi:bell" height="24" />
          <Icon icon="mdi:circle" height="36" />
          <div>Administrator
            <Icon icon="mdi:caret-down" />
          </div>
        </div>
      </nav>
      <div class="base-card-section">
        <div v-for="i in 4">
          <BaseCard class="item" cardTitle="Document" content="146.00" icon="ic:outline-file-copy" delta="12" />
        </div>
      </div>
      <section class="chart-section">
        <div>
          <BarChart />
        </div>
        <div>
          <LineChart />
        </div>
      </section>
    </main>

  </div>
</template>
<script setup lang="ts">
import BaseCard from './components/BaseCard.vue';
import BarChart from './components/BarChart.vue';
import LineChart from './components/LineChart.vue';
import SideNav from './components/SideNav.vue';
import { Icon } from "@iconify/vue"

</script>
<style scoped>
.app-container {
  display: flex;
  column-gap: 0.5rem;
}

.mid-panel {
  width: 100%;
  display: block;
}

.nav-container {
  padding: 0.5rem 0.75rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.base-card-section {
  display: grid;
  grid-template-columns: 25% 25% 25% 25%;
}

.chart-section{
  display: flex;
}

@media (max-width: 1024px) {
  .base-card-section {
    grid-template-columns: 50% 50%;
  }
}

@media (max-width: 768px) {
  .base-card-section {
    grid-template-columns: 100%;
  }
}
</style>