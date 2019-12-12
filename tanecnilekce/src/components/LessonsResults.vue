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
<!--         <p>{{ danceSchool.name }}</p>
        <p>{{ danceSchool.address }}</p>
        <p>{{ danceSchool.tel }}</p>
        <p>{{ lekce.danceFamily }} {{ lekce.style }}</p>
        <p>{{ lekce.daration }} {{ lekce.day }} {{ lekce.time }}</p> -->
        <button>Více o kurzu</button>
      </div> 
    </div>
  </div>
</template>

<script>
export default {
  name: 'lessonsresults',
  components: {
      
  },
  data() {
    return {
      lekce: []
    }
  },
  mounted() {
    fetch('/API/lekce.json')
    .then(response => response.json())
    .then(data => {
      this.lekce = data;
    })
    .catch(error => {
      console.log(error);
    })    
  },
/*   props: [ 'selectedStyle' ], */
  computed () {
    return lekce.filter( kurz => kurz.danceFamily === selectedStyle);
  }
}
</script>






<style>
/* vysledky */
.karticka {
  margin: 10px;
  margin-left: auto;
  margin-right: auto;
  padding: 10px;
  background-color: #f3ebb6;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.5);
  display: flex;
  flex-wrap: wrap;  
}

.karticka a {
  flex-basis: auto;
  margin: 16px 20px 0 16px;
}

.karticka img {
  border-radius: 10%;
}

.detailyNazvy {
  padding-right: 20px;
}

/*///////////////////////// PC ////////////////////////////////*/
@media (min-width: 1100px) {

  .karticka {
  width: 1100px;
 }
}
</style>