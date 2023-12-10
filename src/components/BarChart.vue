<template>
    <div>
        <Bar
        id="Agent Use (Last 20 Games)"
        :options="chartOptions"
        :data="chartData"
        />
    </div>
</template>
  
<script>
import { Bar } from 'vue-chartjs';
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js';
  
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale);
  
export default {
    extends: Bar,
    name: 'AgentUse',
    components: { Bar },
    data() {
        return {
            chartData: {
                labels: ['Jett', 'Killjoy', 'Omen', 'Phoenix', 'Reyna', 'Sage' ],
                datasets: [{ 
                data: [8, 7, 0, 1, 1, 3],
                label:'Games', 
                backgroundColor: 'purple',
                }]
            },
            chartOptions: {
                responsive: true
            }
        }
        }
    }
</script>
