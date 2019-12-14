<template>
  <div class="karticka">
    <div class="detailyNazvy">
      <p>Termín: </p>
      <p>Adresa: </p>
      <p>Taneční škola: </p>
      <p>Lekce: </p>
    </div>

    <div class="detailyVysledky">
      <p>{{ singleGaff.time }}</p>
      <p>{{ singleGaff.address }}</p>
      <p>{{ singleGaff.danceSchool }}</p>
      <p>{{ singleGaff.danceFamily }}</p>
    </div>     
    <button>Více o akci</button>
  </div>  
</template>

<script>
export default {
  name:'gaffsresults',
  components: {

  },
  props: ["singleGaff"]
}
</script>

<style>
.detailyNazvy {
  padding-right: 20px;
}

button {
  color:#280004;
  background-color:#ffffff;
  font-family: 'Roboto Condensed', sans-serif;
  font-size: 16px;
  padding: 10px;
}
</style>