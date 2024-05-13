<template>
    <div class="card-container">
        <div style="display: flex; justify-content: space-between;">
            <p>{{ props.cardTitle }}</p>
            <div class="icon-top-corner">
                <Icon :icon="icon" :ssr="true" color="#1191C6" />
            </div>
        </div>
        <h1>{{ props.content }}</h1>
        <div style="display: flex; column-gap: 1rem; align-items: center;">
            <div style="display: flex; align-items: center; color: green; column-gap: 0.25rem;">
                <Icon icon="fa6-solid:arrow-trend-up" color="green" height="20" /> 
                <div>{{delta}}%</div>
            </div>
            <div style="color: slategrey;">
                <p>Since last week</p>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { Icon } from "@iconify/vue"
const props = defineProps<{
    cardTitle: string,
    content: string,
    icon: string,
    delta:string
}>();
</script>

<style scoped>
/* .card-container {
    margin: 1rem;
    background-color: var(--card-bg);
    padding: 1.25rem;
    border-radius: 25px;
    box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
} */

.icon-top-corner {
    background-color: #E4E9F5;
    font-size: 2rem;
    display: flex;
    align-items: center;
    border-radius: 100%;
    padding: 0.5rem;
}

</style>