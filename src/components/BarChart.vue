<template>
    <div class="card-container">
        <h3>Recent Marketing</h3>
        <Bar id="my-chart-id" :data="chartData" :options="options.options" />
    </div>
</template>

<script setup lang="ts">
import { Bar } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)
const chartData = {
    labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
    datasets: [{
        data: [40, 20, 12, 32, 16, 23, 42, 12, 32, 12, 54, 12],
        backgroundColor: "slateblue",
        labels: "none"
    }]
}
const options = {
    options: {
        scales: {
            x: {
                grid: {
                    display: false
                }
            },
            y: {
                grid: {
                    display: false
                }
            }
        },
        plugins: {
            legend: {
                display: false
            }
        }
    }
}

</script>

<!-- <style scoped>
.card-container {
    margin: 1rem;
    background-color: var(--card-bg);
    padding: 1.25rem;
    border-radius: 25px;
    box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
}
</style> -->