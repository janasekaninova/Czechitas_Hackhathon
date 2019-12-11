<template>
  <div>
    <div class="karticka">
      <a href="http://www.rugcutters.cz/"><img class="logoSkoly" src="@/Images/logo_rugcutters.png" alt="Rug Cutters"></a>
      <div class="detailyNazvy">
        <p>Taneční škola: </p>
        <p>Adresa: </p>
        <p>Kontakt: </p>
        <p>Lekce: </p>
        <p>Termín: </p>
      </div>

      <div class="detailyVysledky">
        <p>Vybraná tš</p>
        <p>její adresa</p>
        <p>její telefon</p>
        <p>čeho lekce</p>
        <p>termín</p>
        <button>Více o kurzu</button>
      </div> 
    </div>
  </div>
</template>

<script>
export default {
  name: 'lessonsresults',
  components: {
      
  }
}
</script>

<style>
/* vysledky */
.karticka {
  background-color: #f3ebb6;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.5);
  margin: 10px;
  padding: 10px;
  display: flex;
  flex-wrap: wrap;     
}

.karticka a {
  flex-basis: 100%;
  margin: 10px 10px 0 0;
}

.karticka img {
  border-radius: 10%;
}

.detailyNazvy {
  padding-right: 20px;
}
</style>