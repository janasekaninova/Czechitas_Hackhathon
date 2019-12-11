<template>
  <div>

    <lessonsresults />

    <ourfooter />
  </div>
</template>

<script>
import LessonsResults from '../components/LessonsResults.vue';
import OurFooter from '../components/OurFooter.vue';
export default {
  name: 'results',
  components: {
    'lessonsresults': LessonsResults,
    'ourfooter': OurFooter
  }
}
</script>

<style>
/*///////////////////////// tablet ////////////////////////////////*/
@media (min-width: 700px) {
  .menu {
    display: flex;
  }

  .menu li {
    border-bottom: 1px solid #ffffff;  
    flex: 0 0 25%;
  }

  .karticka {
    flex-direction: row;
  }

  .karticka a {
    flex-basis: auto;
    margin: 16px 20px 0 16px;
  }
}

/*///////////////////////// PC ////////////////////////////////*/
@media (min-width: 1100px) {
  .menu {
    padding: 50px 150px;
  }
}

</style>