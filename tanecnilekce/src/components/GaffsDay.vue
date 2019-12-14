<template>
  <div>
    <h2>{{ timetable.id }}</h2>
    <gaffsresults 
        v-for="(action, index) in timetable.actions"
        v-bind:singleGaff="action"
        v-bind:key="index"
         />
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
}

</script>

<style>
</style>