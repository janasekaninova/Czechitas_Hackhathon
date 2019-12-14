<template>
  <div>
    <div class="karticka">
      <div class="detailyNazvy">
        <p>Termín: </p>
        <p>Adresa: </p>
        <p>Taneční škola: </p>
        <p>Lekce: </p>
      </div>

      <div class="detailyVysledky">
        <p>termín</p>
        <p>její adresa</p>
        <p>Vybraná tš</p>
        <p>čeho lekce</p>
      </div>     
      <button>Více o akci</button>
    </div>
      
  </div>
  
</template>

<script>
export default {
  name:'gaffsresults',
  components: {

  },
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