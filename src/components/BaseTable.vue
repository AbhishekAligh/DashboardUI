<template>
    <div class="card-container">
        <div style="display: flex; justify-content: space-between; align-items: center; ">
            <div style="display: flex; flex-direction: column; column-gap: 0;">
                <h4 style="margin: 0;padding: 0;"> Document</h4>
                <p style="font-size: x-small;margin: 0.5rem 0;padding: 0; color: slategray;">Documents tracking
                    information</p>
            </div>
            <select name="dropdown">
                <option>Weekly</option>
                <option>Today</option>
                <option>Monthly</option>
            </select>
        </div>

        <table>
            <tr>
                <th>Name</th>
                <th>File</th>
                <th>Category</th>
                <th>Author</th>
                <th>Status</th>
            </tr>
            <tr v-for="row in tableData">
                <td>{{ row.name }}</td>
                <td>{{ row.fileType }}</td>
                <td>{{ row.category }}</td>
                <td>{{ row.author }}</td>
                <td>
                    <div :style="{ background: row.status === 'Send' ? '#CAECD4' : '#FAD9CA', color: row.status === 'Send' ? 'green' : 'red' }"
                        style=" padding: 0.5rem; text-align: center; max-width: 4rem; border-radius: 5px;">
                        {{ row.status }}
                    </div>
                </td>
            </tr>
        </table>
    </div>

</template>

<script setup lang="ts">
import { tableData } from "../data/dummy.ts";
</script>


<style scoped>
table {
    margin: 1rem 0;
    font-family: arial, sans-serif;
    border-collapse: collapse;
    width: 100%;
}

td,
th {
    text-align: left;
    padding: 8px;
}
</style>