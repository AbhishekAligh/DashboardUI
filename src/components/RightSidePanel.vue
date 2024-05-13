<template>
    <aside class="right-side-panel">
        <div>
            <h4>Popular Product</h4>
            <div v-for="item in productList">
                <PanelItem :title="item.title" :subTitle="item.subTitle" />
            </div>
        </div>
        <div>
            <h4>Chat</h4>
            <div v-for="item in chatList">
                <PanelItem :title="item.title" :subTitle="item.subTitle" />
            </div>
        </div>
    </aside>
</template>
<script setup lang="ts">
import PanelItem from './PanelItems.vue'
import { chatList, productList } from "../data/dummy.ts";
</script>
<style scoped>
.right-side-panel {
    display: none;
}

@media (min-width: 1024px) {
    .right-side-panel {
        display: flex;
        flex-direction: column;
        row-gap: 2rem;
        height: 70vh;
        border-radius: 15px;
        background-color: white;
        min-width: 10vw;
        padding: 1rem;
        margin: 0.75rem 0.5rem;
    }

    h4 {
        margin: 0;
    }
}
</style>