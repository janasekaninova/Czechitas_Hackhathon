<template>
  <div>
    <div class="tancirnyUvod">
    Už toho umíš dost a chceš si jenom zatančit, nebo se nanejvýš naučit nějaký ten pohyb navíc? Od toho tu jsou tančírny, kde za drobný peníz získáš prostor na parketu a třeba i radu zkušenějších.
    </div>

    <div>
      <gaffsday />
<!--       <h2>Pondělí</h2>
        <gaffsresults />
      <h2>Úterý</h2>
        <gaffsresults />
      <h2>Středa</h2>
        <gaffsresults />
      <h2>Čtvrtek</h2>
        <gaffsresults />
      <h2>Pátek</h2>
        <gaffsresults />
      <h2>Sobota</h2>
        <gaffsresults />
      <h2>Neděle</h2>
        <gaffsresults /> -->
    </div>

    <ourfooter />
  </div>
</template>

<script>
/* import GaffsResults from '../components/GaffsResults'; */
import GaffsDay from '../components/GaffsDay';
import OurFooter from '../components/OurFooter.vue';
export default {
  name: 'gaffs',
  components: {
/*     'gaffsresults': GaffsResults, */
    'gaffsday': GaffsDay,
    'ourfooter': OurFooter   
  }
}
</script>

<style>
h2 {
  padding: 20px;
  margin: 5px;
}

h3 {
  padding: 0 50px;
}

p {
  padding: 0 30px;
}

.tancirnyUvod {
  font-size: 22px;
  padding: 20px 40px;
  text-align: center;
}

/*///////////////////////// tablet ////////////////////////////////*/
@media (min-width: 700px) {
  .menu {
    display: flex;
  }

  .menu li {
    border-bottom: 1px solid #ffffff;  
    flex: 0 0 25%;
  }
}

/*///////////////////////// PC ////////////////////////////////*/
@media (min-width: 1100px) {
  .menu {
    padding: 50px 150px;
  }
}
</style>