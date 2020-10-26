<template>
  <div class="container align-items-center justify-content-center d-flex text-center"
       style="min-height: 100vh">

    <div class="card">
      <div class="card-header">Skladba má chybějícího autora</div>

      <div class="card-body">
        <p>Kdo je autorem skladby Víc lásky?</p>

        <input placeholder="picker">

        <div class="mt-3">

          <a class="btn btn-secondary">Přeskočit</a> <a class="btn btn-primary">Uložit</a>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: "author"
}
</script>

<style scoped>

</style>
