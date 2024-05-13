<template>
  <div class="app-container">
    <SideNav />
    <main class="mid-panel">
      <nav class="nav-container">
        <div style="display: flex; align-items: center; column-gap:1rem;">
          <Icon icon="gravity-ui:bars" height="1.5rem" class="hamburger-icon" />
          <h1>Overview</h1>
        </div>
        <div>
        </div>
        <div style="display: flex; column-gap: 0.5rem; align-items: center; ">
          <Icon icon="ph:bell-bold" height="24" />
          <Icon icon="carbon:user-avatar-filled-alt" height="36" color="orange" />
          <div>Administrator
            <Icon icon="mdi:caret-down" />
          </div>
        </div>
      </nav>
      <div style="display: flex; justify-content: space-between;">
        <div style="flex-grow: 3;">
          <section class="base-card-section">
            <div v-for="item in baseCardList">
              <BaseCard class="item" :cardTitle="item.cardTitle" :content="item.content" :icon="item.icon"
                :delta="item.delta" />
            </div>
          </section>
          <section class="chart-section">
            <div>
              <LineChart />
            </div>
            <div>
              <BarChart />
            </div>
          </section>
          <section class="table-section">
            <BaseTable />
          </section>
        </div>
        <RightSidePanel />
      </div>
    </main>
  </div>
</template>
<script setup lang="ts">
import RightSidePanel from './components/RightSidePanel.vue';
import BaseCard from './components/BaseCard.vue';
import BaseTable from './components/BaseTable.vue';
import BarChart from './components/BarChart.vue';
import LineChart from './components/LineChart.vue';
import SideNav from './components/SideNav.vue';
import { Icon } from "@iconify/vue"
import { baseCardList } from './data/dummy.ts'

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
  padding: 1rem 0.75rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.base-card-section {
  display: grid;
  grid-template-columns: 25% 25% 25% 25%;
}

.chart-section {
  display: grid;
  grid-template-columns: 50% 50%;
}

.table-section {
  display: grid;
  grid-template-columns: 100%;
}

.hamburger-icon {
  display: none;
}

@media (max-width: 1024px) {
  .base-card-section {
    grid-template-columns: 50% 50%;
  }

  .hamburger-icon {
    display: inline-block;
  }
}


@media (max-width:768px) {
  .card-container {
    margin: 0.5rem;
  }


  .chart-section {
    grid-template-columns: 100%;
  }
}
</style>