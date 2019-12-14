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
  mounted() {
      fetch('/API/tancirny.json')
      .then(response => response.json())
      .then(data => {
          this.osoby = data.results;
          this.loading = false;
      })
      .catch(error => {
          console.log(error);
      })    
    }
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