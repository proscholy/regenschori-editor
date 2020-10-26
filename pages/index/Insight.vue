<template>
  <div class="row align-items-center">
    <div class="col-6">

      <p class="mb-2 title">{{ title }}</p>

      <div class="progress rounded"
           style="height: 26px">
        <div class="progress-bar rounded"
             role="progressbar"
             :style="'width: 45%; background-color:' + color"
             aria-valuenow="25"
             aria-valuemin="0"
             aria-valuemax="100"><span><b style="float: right; padding-right: 20px;">45%</b></span></div>
      </div>
    </div>
    <div class="col-3 text-right">
      <span class="small">Zbývá doplnit 45 záznamů</span>
    </div>
    <div class="col-3">
      <nuxt-link class="btn btn-success rounded py-2 px-4" to="author">Doplnit</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Insight",

  props: [
    'title', 'color'
  ]
}
</script>

<style scoped>

.row {
  padding:       18px 0;

  border-bottom: 1px solid #eeeeee;
}


.title {
  font-weight: 600;
  font-size:   1.2em;
  color:       #2f2f2f;
}


.rounded {
  border-radius: 50px !important;
}


.progress-bar span {
  text-align:     left;
  padding-left:   20px;
  letter-spacing: 0.125em;
  font-weight:    bold;
  font-size:      1.25em;
}


.progress-bar {}


.btn-success {
  background-color: #112362;
  border-color:     #112362;

}
</style>
