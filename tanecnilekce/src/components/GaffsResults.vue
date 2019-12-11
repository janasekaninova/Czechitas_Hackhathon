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

    }
}
</script>

<style>
    .karticka {
  background-color: #f3ebb6;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.5);
  margin: 10px;
  padding: 10px;
  display: flex;
  flex-wrap: wrap;     
}

.detailyNazvy {
  padding-right: 20px;
}
</style>