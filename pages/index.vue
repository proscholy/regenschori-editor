<template>
  <div>
    <div class="row">
      <div class="col-sm-9">
        Pomocí tohoto rozhraní lze doplňovat obsah do databáze Regenschori.cz.

        <h2 class="mt-3">Skladby</h2>

        <div class="insight-wrapper material-shadow">

          <insight title="Autor"
                   color="#112362"></insight>

          <insight title="Štítky"
                   color="#00498D"></insight>

          <insight title="Text"
                   color="#00486f"></insight>

          <insight title="Akordy"
                   color="#0070AD"></insight>

          <insight title="Noty (LilyPond)"
                   color="#149ae2"></insight>

        </div>

        <h2 class="mt-4">Materiály</h2>

        <div class="insight-wrapper material-shadow">
          <insight title="Skladby s doplněnou nahrávkou"></insight>
        </div>


      </div>

      <div class="col-sm-3">
        <profile/>

      </div>


    </div>

  </div>
</template>

<script>
import Insight from "@/pages/index/Insight";
import Profile from "@/pages/index/Profile";

export default {
  components: {Profile, Insight}
}
</script>

<style>
.insight-wrapper {

  padding:       0 2em;

  border-radius: 5px;
}
</style>
