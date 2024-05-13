<template>
    <div style="display: flex; column-gap: 0.5rem; align-items: center; margin: 1rem 0;">
        <Icon icon="mdi:circle" height="36" />
        <div style="display: flex; flex-direction: column; column-gap: 0;">
            <p style="margin: 0;padding: 0;"> {{ props.title }}</p>
            <p style="font-size: x-small;margin: 0;padding: 0; color: slategray;">${{ props.subTitle }}</p>
        </div>
    </div>
</template>

<script setup lang="ts">
import { Icon } from '@iconify/vue'
const props = defineProps<{
    title: string,
    subTitle: string
}>()
</script>

<style scoped></style>