<template>
  <div class="home">
    <!-- vyhledávací formulář-->
    <div class="formular" id="app">
      <h2>Chci najít lekce</h2>
      <label for="mesto">Lokalita</label>
        <select name="mesto" id="mesto">
          <option value="">Vyberte městskou část</option>
          <option value="1">Bohunice</option>
          <option value="2">Bosonohy</option>
          <option value="3">Bystrc</option>
          <option value="3">Černovice</option>
          <option value="3">Chrlice</option>
          <option value="3">Ivanovice</option>
          <option value="3">Jehnice</option>
          <option value="3">Jih</option>
          <option value="3">Jundrov</option>
          <option value="3">Kníničky</option>
          <option value="3">Kohoutovice</option>
          <option value="3">Komín</option>
          <option value="3">Královo Pole</option>
          <option value="3">Líšeň</option>
          <option value="3">Maloměřce a Obřany</option>
          <option value="3">Medlánky</option>
          <option value="3">Nový Lískovec</option>
          <option value="3">Ořešín</option>
          <option value="3">Řečkovice a Mokrá Hora</option>
          <option value="3">Sever</option>
          <option value="3">Slatina</option>
          <option value="3">Starý Lískovec</option>
          <option value="3">Střed</option>
          <option value="3">Tuřany</option>
          <option value="3">Útěchov</option>
          <option value="3">Vinohrady</option>
          <option value="3">Žabovřesky</option>
          <option value="3">Žebětín</option>
          <option value="3">Židenice</option>
        </select>
      <br>

      <label for="styl">Styl tance</label>
        <select name="styl" id="styl">
          <option value="">Vyberte styl</option>
          <option value="1">Swing</option>
          <option value="2">Latina</option>
          <option value="3">Standard</option>
        </select>
      <br>

      <fieldset>
        <legend >Jaký den mi vyhovuje?</legend>
        <br>
        <div class="dny">
          <input type="checkbox" id="pondeli" name="pondeli">
          <label for="scales">Pondělí</label>
          <br>
          <input type="checkbox" id="utery" name="utery">
          <label for="scales">Úterý</label> 
          <br>
          <input type="checkbox" id="streda" name="streda">
          <label for="scales">Středa</label>
          <br>
          <input type="checkbox" id="ctvrtek" name="ctvrtek">
          <label for="scales">Čtvrtek</label>
          <br>
          <input type="checkbox" id="patek" name="patek">
          <label for="scales">Pátek</label>
          <br>                
          <input type="checkbox" id="sobota" name="sobota">
          <label for="scales">Sobota</label>
          <br>
          <input type="checkbox" id="nedele" name="nedele">
          <label for="scales">Neděle</label>
          <br>
        </div>
      </fieldset>

      <button type="button">Vyhledat</button>

    </div>

    <!-- fotogalerie -->
    <section class="fotogalerie">
      <a href="https://www.danza.cz/"><img src="@/Images/logo_danza.png" alt="logo TŠ Danza"></a>
      <a href="https://tsdynamic.cz/"><img src="@/Images/logo_dynamic.png" alt="logo TŠ Dynamic"></a>
      <a href="https://www.tanecniskolaeso.cz/"><img src="@/Images/logo_eso.png" alt="logo TŠ Eso"></a>
      <a href="http://www.rugcutters.cz/"><img src="@/Images/logo_rugcutters.png" alt="logo TŠ Rug Cutters"></a>
      <a href="https://www.starlet-brno.cz/"><img src="@/Images/logo_starlet.png" alt="logo TŠ Starlet"></a>
      <a href="http://studiostolarna.cz/stolarna/index.php"><img src="@/Images/logo_stolarna.png" alt="logo TŠ Stolárna"></a>
      <a href="https://www.swingwings.cz/"><img src="@/Images/logo_swing_wings.png" alt="logo TŠ Swing Wings"></a>
    </section>

    <ourfooter />

  </div>
</template>

<script>
import OurFooter from '../components/OurFooter.vue';
export default {
  name: 'home',
  components: {
    'ourfooter': OurFooter
  }
}
</script>

<style>
/* vyhledávací formulář */
h2 {
    font-size: 36px;
    margin-top: 5px;
}

label,
legend {
  font-size: 22px;
  margin: 5px;
}

fieldset {
  padding: 5px;
}

.formular {
  padding: 10px;
  margin: 10px;
  margin-left: auto;
  margin-right: auto;
  background-color: #f3ebb6;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.5);
}

button {
  color:#280004;
  background-color:#ffffff;
  font-family: 'Roboto Condensed', sans-serif;
  font-size: 16px;
  font-weight: bold;
  padding: 10px;
}

/* fotogalerie */
.fotogalerie {
  justify-content: space-between;
  align-items: center;
  display: flex;
  flex-flow: row wrap;
  padding: 40px;
}

.fotogalerie img {
  filter: grayscale(100%);
  transition: 0.4s;
}

.fotogalerie img:hover {
  filter: grayscale(0);
} 

/*///////////////////////// tablet ////////////////////////////////*/
@media (min-width: 700px) {
  .menu {
    display: flex;
  }

  .menu li {
    border-bottom: 1px solid #ffffff;  
    flex: 0 0 33%;
  }

  .dny {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
  }
}

/*///////////////////////// PC ////////////////////////////////*/
@media (min-width: 1100px) {
  .menu {
    padding: 50px 150px;
  }

  .formular {
  width: 1100px;
 }
}
</style>
