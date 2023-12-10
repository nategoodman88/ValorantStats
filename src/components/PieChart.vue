<template>
    <div>
        <Pie
        id="WinLose"
        :data="data"
        :options="options" 
        />
    </div>
</template>
  
<script>
import { Pie } from 'vue-chartjs';
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'

ChartJS.register(ArcElement, Tooltip, Legend)

  
export default {
    extends: Pie,
    name: 'WinLose',
    components: { Pie },
    data() {
        return {
            data: {
                labels: ['Win', 'Lose'],
                datasets: [{       
                    backgroundColor: ['green', 'red'],
                    data: [9, 11]
                }]  
            },
            options: {
                responsive: true,
            }
        }
     }
  }
 </script>