<template>
  <div id="app2">
    <p>{{ message }}</p>
    <table>
      <colgroup>
        <col>
        <col>
        <col>
      </colgroup>
      <tr>
        <td></td>
        <td>
          <label for="inflow-rate">Inflow Rate</label>
          <input id="inflow-rate" v-model="inflow_rate">
        </td>
        <td></td>
      </tr>
      <tr>
        <td>
          <label for="source-rate">Source Rate</label>
          <input id="source-rate" v-model="source_rate">
        </td>
        <td>
          <div id="summary">
            <p>
              Inflow Rate: {{ inflow_rate }}<br>
              Source Rate: {{ source_rate }}<br>
              Drain Rate: {{ drain_rate }}<br>
              Outflow Rate: {{ outflow_rate }}<br>
            </p>
          </div>
        </td>
        <td>
          <label for="drain-rate">Drain Rate</label>
          <input id="drain-rate" v-model="drain_rate">
        </td>
      </tr>
      <tr>
        <td></td>
        <td>
          <label for="outflow-rate">Outflow Rate</label>
          <input id="outflow-rate" v-model="outflow_rate">
        </td>
        <td></td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      message: "Hello Vue!",
      outflow_rate: 100,
      inflow_rate: 100,
      source_rate: 100,
      drain_rate: 100
    }
  }
}
</script>

<style scoped>
p {
  font-size: 2em;
  text-align: center;
}
</style>
