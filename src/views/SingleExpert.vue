<template>
  <div class="single-expert pa-5">
    <div class="row">
      <div class="col-12 head pa-5">
        <h1>{{this.$route.query.name}}</h1>
      </div>
      <hr>
      <div class="col-12 chart">
          <div id="chart">
            <apexchart width="500" type="line" :options="chartOptions" :series="series"></apexchart>
          </div>
      </div>
    </div>
  </div>

</template>

<script>

export default {
  name: 'hello',
  data() {
    return{
      chartOptions: {
        chart: {
          id: 'vuechart-example'
        },
        xaxis: {
          categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul'],
        }
      },
      series: [{
        name: 'trade',
        data: [10, -22.4, -12.3, 21.5, 15.8, 40, 33.7]
      }]
    }
  },
}

</script>

<style scoped>
.chart__container {
  width: 40%;
  margin: auto;
  background: white;
}
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>