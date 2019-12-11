<template>
  <div id="app">
    <link href="https://fonts.googleapis.com/css?family=Roboto+Condensed:300,400,700&display=swap&subset=latin-ext" rel="stylesheet">
    <header>
      <h1 class="titulek">Taneční kurzy a kde je najít</h1>
      <img class="logo" src="@/Images/logo.jpg">
      <p class="perex">Chceš začít tančit, ale nevíš kudy do toho? Pomůžeme ti s prvními krůčky - řekni nám, čemu se chceš věnovat a my ti ukážeme nabídku otevřených kurzů v okolí.</p>
      <section class="listaMenu">
            <ul class="menu">
              <router-link to="/">Úvod</router-link>
              <router-link to="/results">Výsledky</router-link>
              <router-link to="/dances">Tance</router-link>
              <router-link to="/gaffs">Tančírny</router-link>
              <router-link to="/about">O nás</router-link>
            </ul>
      </section>
    </header>

    <router-view/>

  </div>
</template>

<script>
export default {
  name: 'app',
  components: { 
  }
}
</script>

<style>
body {
    font-family: 'Roboto Condensed', sans-serif;
    padding: 0;
    margin: 0;
}

/* hlavicka */
header {
    background-image: 
        linear-gradient(to bottom,rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)),
        url("/Images/mitchell-griest-EKXCGy4Zsbg-unsplash.jpg");
    background-repeat: no-repeat;
    background-size: 100%, cover;
    background-position: center;
    text-align: center;
    color: #f5f5f5;
    padding: 60px 0 0 0;
}

.titulek {
    margin: 50px 10px;
    font-size: 42px;
}

.logo {
    border-radius: 50%;
    padding: 0;
}

.perex {
    padding: 10px 40px;
    font-size: 18px;
}

/* menu */
.menu {
    list-style: none;
    text-transform: uppercase;
    /* text-align: center; */
    font-size: 22px;
    padding: 50px;
    margin: 0;
}

.menu a {
    color: #ffffff;
    text-decoration: none;
    display: block;
    padding: 7px 0px;
    border-bottom: 0.2px solid #ffffff;
}

/* paticka */
footer {
    color: white;
    background-color: #280004; 
    padding: 15px;
    font-size: small;
}

footer a {
    color: white;
    font-weight: normal;
}

/*///////////////////////// tablet ////////////////////////////////*/
@media (min-width: 700px) {
    .menu {
        display: flex;
        justify-content: center;
    }

    .menu a {
        border-bottom: 1px solid #ffffff;  
        flex: 0 0 20%;
    }

    .dny {
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
    }

    fieldset {
        padding: 0;
    }
}

/*///////////////////////// PC ////////////////////////////////*/
@media (min-width: 1100px) {
    .menu {
        padding: 50px 150px;
    }
}


/* #nav a.router-link-exact-active {
  color: #42b983;
} */
</style>
