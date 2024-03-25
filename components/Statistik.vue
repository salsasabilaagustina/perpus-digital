<template>
    <div>
        <canvas id="myChart"></canvas>
    </div>
</template>

<script setup>
import Chart from 'chart.js/auto';

const labels=[
    'january',
    'february',
    'march',
    'april',
    'may',
    'june',
    
];

const data= {
    labels : labels,
    datasets: [{
        label: 'Pengunjung',
        backgroundColor: 'rgb(255, 99, 132)',
        borderColor: 'rgb(255, 99, 132)',
        data: [30, 10, 5, 10, 20, 30, 5],
    }]
};

const config = {
    type: 'bar',
    data: data,
    options: {}
};

onMounted(()=>{
    const myChart = new Chart(
    document.getElementById('myChart'),
    config
);
})
</script>