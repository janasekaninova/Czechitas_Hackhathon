<template>
  <div>
    <h2>nadpis dne</h2>

    <gaffsresults />
  </div>
</template>

<script>
import GaffsResults from "./GaffsResults.vue";
export default {
  name: "gaffsday",
  components: {
    gaffsresults: GaffsResults
  },

  props: ["timetable"]
};
</script>

<style>
</style>