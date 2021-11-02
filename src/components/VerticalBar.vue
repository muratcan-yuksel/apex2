<template>
  <div>
    <apexchart
      width="500"
      type="bar"
      :options="chartOptions"
      :series="series"
    ></apexchart>
  </div>
</template>

<script>
// you can import in a particular component and register the component like below
import VueApexCharts from "vue3-apexcharts";
export default {
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      chartOptions: {
        theme: {
          mode: "dark",
          palette: "palette6",
          monochrome: {
            enabled: false,
            color: "#A5978B",
            shadeTo: "dark",
            shadeIntensity: 0.65,
          },
        },
        chart: {
          id: "vuechart-example",
        },
        // theme: {
        //   palette: "palette8", // upto palette10
        // },
        xaxis: {
          categories: [
            "Javascript",
            "HTML/CSS",
            "Python",
            "SQL",
            "JAVA",
            "Node.js",
            "TypeScript",
            "C#",
          ],
        },
      },
      series: [
        {
          name: "series-1",
          data: [64.96, 56.07, 48.24, 47, 35, 33, 30, 27],
          // colors: ["#546E7A", "#E91E63"],
        },
      ],
    };
  },
};
</script>

<style></style>
