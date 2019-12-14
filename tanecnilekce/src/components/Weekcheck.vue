<template>
  <fieldset>
    <legend >Jaký den mi vyhovuje?</legend>
    <div class="checkboxArea">
      <div class="days">
        <input type="checkbox" id="monday" name="monday" value="monday" v-model="checkedDay">
        <label for="monday">Pondělí</label>
      </div>
      <div class="days">
        <input type="checkbox" id="tuesday" name="tuesday" value="tuesday" v-model="checkedDay">
        <label for="thuesday">Úterý</label> 
      </div>
      <div class="days">
        <input type="checkbox" id="wednesday" name="wednesday" value="wednesday" v-model="checkedDay">
        <label for="wednesday">Středa</label>
      </div>
      <div class="days">
        <input type="checkbox" id="thursday" name="thursday" value="thursday" v-model="checkedDay">
        <label for="thursday">Čtvrtek</label>
      </div>
      <div class="days">
        <input type="checkbox" id="friday" name="friday" value="friday" v-model="checkedDay">
        <label for="friday">Pátek</label>
      </div>
      <div class="days">
        <input type="checkbox" id="saturday" name="saturday" value="saturday" v-model="checkedDay">
        <label for="saturday">Sobota</label>
      </div>
      <div class="days">
        <input type="checkbox" id="sunday" name="sunday" value="sunday" v-model="checkedDay">
        <label for="sunday">Neděle</label>
      </div>
    </div>
  </fieldset>
</template>



<script>
export default {
  name: 'weekcheck',
  data() {
    return {
      checkedDay: []
    }
  },
  watch: {
    checkedDay: function (value) {
      this.$emit('dayFilterChange', value);
    }
  }
}
</script>



<style>
legend {
  font-size: 22px;
  margin: 5px;
  padding: 5px;
}

fieldset {
  padding: 5px;
}
/*///////////////////////// tablet ////////////////////////////////*/
@media (min-width: 700px) {
    .checkboxArea {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
}
</style>