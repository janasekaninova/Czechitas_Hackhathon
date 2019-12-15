<template>
  <div class="karticka">
    <a href="http://www.rugcutters.cz/">
      <img class="logoSkoly" src="@/Images/logo_rugcutters.png" alt="Rug Cutters" />
    </a>
    <div class="detailyNazvy">
      <p>Taneční škola:</p>
      <p>Adresa:</p>
      <p>Kontakt:</p>
      <p>Lekce:</p>
      <p>Termín:</p>
    </div>

    <div class="detailyVysledky">
      {{ cardContent }}
      <button>Více o kurzu</button>
      <div class="detailyVysledky">
        <p>{{ cardContent.danceSchool}}</p>
        <p>{{ cardContent.address }}</p>
        <p>{{ cardContent.tel }}, {{ cardContent.email }}</p>
        <p>{{ cardContent.style }}, {{ cardContent.level }}</p>
        <p>{{ cardContent.duration }}, {{ cardContent.day }}, {{ cardContent.time }}</p>
      </div>
      <button>Více o kurzu</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "cardresults",
  props: ["cardContent"]
};
</script>

<style>
.karticka {
  margin-top: 10px;
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
    max-width: 1100px;
  }
}
</style>