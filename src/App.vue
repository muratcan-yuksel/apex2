<template>
  <h1>Charts and stuff</h1>
  <h2>Vertical bar & most used techs</h2>
  <div id="vertical">
    <VerticalBar />
  </div>
  <div id="stackNdonut">
    <div id="stacked">
      <Stacked />
    </div>
    <div id="donut">
      <Donut />
    </div>
  </div>
  <!-- <BarChart /> -->
  <!-- <div>home</div> -->
</template>

<script>
import VerticalBar from "./components/VerticalBar.vue";
// import BarChart from "./components/BarChart.vue";
import Stacked from "./components/Stacked.vue";
import Donut from "./components/Donut.vue";
export default {
  name: "App",
  components: {
    VerticalBar,
    // BarChart,
    Stacked,
    Donut,
  },
};
</script>

<style>
/* div {
  color: red;
} */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  /* background-color: rgb(190, 177, 177); */
}
#vertical {
  display: flex;
  justify-content: center;
  align-items: center;
  /* border-bottom: 2px solid black; */
}
#stackNdonut {
  display: flex;
  /* justify-content: space-around; */
  align-items: center;
  flex-wrap: wrap;
}
</style>
