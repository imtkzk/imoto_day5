<template>
  <div class="container">
    <h1 class="mt-5">Nuxtでvue-ChartJsを使ってみよう！</h1>
    <div class="row">
      <div class="col-md-4 py-5">
        <line-chart :chartdata="chartdata01" :options="options01" />
      </div>
      <div class="col-md-4 py-5">
        <bar-chart :chartdata="chartdata02" :options="options02" />
      </div>
      <div class="col-md-4 py-5">
        <line-chart02 />
      </div>
      <div class="col-md-4 py-5">
        <pie-chart :chartdata="chartdata03" :options="options03" />
      </div>
      <div class="col-md-4 py-5">
        <radar-chart :chartdata="chartdata04" :options="options04" />
      </div>
    </div>
  </div>
</template>

<script>
import LineChart from "~/components/LineChart.vue";
import BarChart from "~/components/BarChart.vue";
import PieChart from "~/components/PieChart.vue";
import RadarChart from "~/components/RadarChart.vue";
import LineChart02 from "~/plugins/LineChart02.js";

export default {
  components: {
    LineChart,
    BarChart,
    PieChart,
    RadarChart,
    LineChart02
  },
  data() {
    return {
      chartdata01: {
        labels: ["January", "February"],
        datasets: [
          {
            label: ["January"],
            backgroundColor: "#f87979",
            data: [40, 30]
          }
        ]
      },
      options01: {
        responsive: true,
        maintainAspectRatio: false
      },
      chartdata02: {
        labels: ["January", "February"],
        datasets: [
          {
            label: ["January"],
            backgroundColor: "#f87979",
            data: [40, 30]
          }
        ]
      },
      options02: {
        responsive: true,
        maintainAspectRatio: false
      },

      chartdata03: {
        labels: ["January", "February"],
        datasets: [
          {
            label: ["January"],
            backgroundColor: "#f87979",
            data: [40, 30]
          }
        ]
      },
      options03: {
        responsive: true,
        maintainAspectRatio: false
      },

      chartdata04: {
        labels: ["攻撃力", "知力", "すばやさ"],
        datasets: [
          {
            label: "Scouter",
            backgroundColor: "#f87979",
            data: [10780, 87010, 3927]
          }
        ]
      },
      options04: {
        responsive: true,
        maintainAspectRatio: false
      }
    };
  }
};
</script>
