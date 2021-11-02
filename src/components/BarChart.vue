<template id="barchart">
  <div id="chart">
    <apexchart
      type="bar"
      height="350"
      :options="chartOptions"
      :series="series"
    ></apexchart>
  </div>
</template>
<script>
// you can import in a particular component and register the component like below
import VueApexCharts from "vue3-apexcharts";
export default {
  name: "barChart",
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      series: [
        {
          data: [400, 430, 448, 470, 540],
        },
      ],
      chartOptions: {
        chart: {
          type: "bar",
          height: 250,
        },
        colors: ["#5C4742", "#A5978B", "#8D5B4C", "#5A2A27", "#C4BBAF"],
        plotOptions: {
          bar: {
            borderRadius: 4,
            horizontal: true,
          },
        },
        dataLabels: {
          enabled: false,
        },
        xaxis: {
          categories: [
            "South Korea",
            "Canada",
            "United Kingdom",
            "Netherlands",
            "Italy",
          ],
        },
      },
    };
  },
};
</script>
<style scoped>
div {
  background-color: blue;
  border: 1px solid red;
}
#chart {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
