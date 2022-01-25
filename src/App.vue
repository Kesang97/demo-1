<template>
  <div id="app">
    <p>
      hello <strong>{{ name }}</strong
      >,
    </p>
    <p>
      we are extremely delighted to have you on board. Your position in our
      company will be <strong>full time intern</strong>
    </p>
    <p>best wishes for your future endeavours.</p>
    <table>
      <tr v-for="(data, index) in data" :key="index">
        <td>
          {{ data.name }}
        </td>
        <td>
          {{ data.marks }}
        </td>
        <td>
          {{ checkRes(data.marks) }}
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Keshang Sherpa",
      data: [
        { name: "Keshang", marks: 77 },
        { name: "ashutosh", marks: 45 },
        { name: "karan", marks: 41 },
        { name: "rabin", marks: 99 },
      ],
    };
  },
  methods: {
    checkRes(m) {
      if (m > 70) {
        return "excellent";
      } else {
        return "average";
      }
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
