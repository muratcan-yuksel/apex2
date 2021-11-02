<template>
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
  name: "stacked",
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      series: [
        {
          name: "Loved",
          data: [86, 81, 73, 72, 70, 68],
        },
        {
          name: "Dreaded",
          data: [14, 19, 27, 28, 30, 32],
        },
      ],
      chartOptions: {
        chart: {
          type: "bar",
          height: 350,
          stacked: true,
          stackType: "100%",
        },
        theme: {
          mode: "light",
          palette: "palette5",
          monochrome: {
            enabled: false,
            color: "#255aee",
            shadeTo: "dark",
            shadeIntensity: 0.65,
          },
        },
        plotOptions: {
          bar: {
            horizontal: true,
          },
        },
        stroke: {
          width: 1,
          colors: ["#fff"],
        },
        title: {
          text: "100% Stacked Bar",
        },
        xaxis: {
          categories: [
            "Rust",
            "Clojure",
            "TypeScript",
            "Elixir",
            "Julia",
            "Python",
          ],
        },
        tooltip: {
          y: {
            formatter: function (val) {
              return val + "K";
            },
          },
        },
        fill: {
          opacity: 1,
        },
        legend: {
          position: "top",
          horizontalAlign: "left",
          offsetX: 40,
        },
      },
    };
  },
};
</script>
<style scoped>
/* div {
  background-color: blue;
  border: 1px solid red;
}
#chart {
  display: flex;
  justify-content: center;
  align-items: center;
} */
</style>
