<template>
    <div class="card-container">
        <h3>Recent Marketing</h3>
        <div style="display: flex; color: green; column-gap: 0.25rem;">
            <div  style="display: flex; column-gap: 0.25rem;">
                <Icon icon="fa6-solid:arrow-trend-up" color="green" height="20" /> <div>16%</div>
            </div>
            <Bar id="my-chart-id" class="canvas-container" :data="chartData" :options="options.options" />
        </div>
    </div>
</template>

<script setup lang="ts">
import {Icon} from '@iconify/vue'
import { Bar } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)
const chartData = {
    labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
    datasets: [{
        data: [40, 20, 12, 32, 16, 23, 42, 12, 32, 12, 54, 12],
        backgroundColor: "#1291C2",
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
                display: false,
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

