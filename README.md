<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Raneesha Portfolio Charts</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body {
      background: #0d1117;
      color: white;
      font-family: Arial;
      text-align: center;
    }
    .chart-container {
      width: 400px;
      margin: 40px auto;
    }
  </style>
</head>
<body>

<h2>🍩 Dashboards by Platform</h2>
<div class="chart-container">
  <canvas id="donutChart"></canvas>
</div>

<h2>📊 Work by Software</h2>
<div class="chart-container">
  <canvas id="barChart"></canvas>
</div>

<script>
const donut = new Chart(document.getElementById('donutChart'), {
    type: 'doughnut',
    data: {
        labels: ['R Shiny', 'Power BI', 'Excel'],
        datasets: [{
            data: [1, 1, 1],
            backgroundColor: ['#36A2EB', '#FF6384', '#FFCE56']
        }]
    }
});

const bar = new Chart(document.getElementById('barChart'), {
    type: 'bar',
    data: {
        labels: ['Excel', 'Power BI', 'SPSS', 'STATA', 'R'],
        datasets: [
            {
                label: 'Dashboards',
                data: [1, 1, 0, 0, 1],
                backgroundColor: '#36A2EB'
            },
            {
                label: 'Assignments',
                data: [1, 1, 1, 1, 0],
                backgroundColor: '#FF6384'
            }
        ]
    },
    options: {
        responsive: true,
        plugins: {
            legend: {
                labels: { color: 'white' }
            }
        },
        scales: {
            x: {
                ticks: { color: 'white' }
            },
            y: {
                ticks: { color: 'white' }
            }
        }
    }
});
</script>

</body>
</html>
