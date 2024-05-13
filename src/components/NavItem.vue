<template>
    <div class="nav-item">
        <Icon :icon="props.icon" height="20px" />
        <p>{{ props.title }}</p>
    </div>
</template>

<script setup lang="ts">
import { Icon } from '@iconify/vue'
const props = defineProps<{
    title: string,
    icon: string
}>()
</script>

<style scoped>
p {
    margin: 0;
}

.nav-item:hover {
    color: white;
    background-color: #3963AD;
}

.nav-item {
    display: flex;
    align-items: center;
    column-gap: 0.5rem;
    padding: 0.75rem;
    border-radius: 15px;
    color:#7A9BC4;
    font-size: 14px;
}
</style>