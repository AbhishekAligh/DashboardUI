<template>
    <div class="card-container">
        <h3>Recent Workflow</h3>
        <div style="display: flex; color: green; column-gap: 0.25rem;">
            <div>
                <Icon icon="fa6-solid:arrow-trend-up" color="green" height="20" /> 16%
            </div>
                <Line class="canvas-container" :data="data" :options="options.options" />
            </div>
    </div>

</template>
<script setup lang="ts">
import {
    Chart as ChartJS,
    CategoryScale,
    LinearScale,
    PointElement,
    LineElement,
    Title,
    Tooltip,
    Legend,
} from 'chart.js'
import { Line } from 'vue-chartjs'
ChartJS.register(
    CategoryScale,
    LinearScale,
    PointElement,
    LineElement,
    Title,
    Tooltip,
    Legend
)

const data = {
    labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
    datasets: [
        {
            label: 'Data One',
            backgroundColor: '#1291C2',
            borderColor:'#1291C2',
            data: [40, 20, 12, 32, 16, 23, 42, 12, 32, 12, 54, 12],
        }
    ],
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
                display:false,
                grid: {
                    display: false
                }
            }
        }, plugins: {
            legend: {
                display: false
            }
        }
    }
}
</script>


<style scoped></style>