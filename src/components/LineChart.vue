<template>
    <div class="card-container">
        <h3>Recent Workflow</h3>
        <Line :data="data" :options="options.options" />
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
            backgroundColor: 'red',
            data: [40, 39, 10, 40, 39, 80, 40]
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