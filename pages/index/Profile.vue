<template>
  <div class="card material-shadow">
    <div class="card-body text-center">

      <img src="~/assets/profile.jpg"
           class="avatar rounded-circle"
           alt="">

      <p class="title mt-2 mb-0">Michael</p>
      <p class="points small">25 b.</p>

<div class="row">
  <div class="col-6">
    <p class="small">12 přidaných autorů</p>
  </div>
  <div class="col-6">
    <p class="small">12 přidaných autorů</p>
  </div>
  <div class="col-6">
    <p class="small">12 přidaných autorů</p>
  </div>
  <div class="col-6">
    <p class="small">12 přidaných autorů</p>
  </div>
  <div class="col-6">
    <p class="small">12 přidaných autorů</p>
  </div>
  <div class="col-6">
    <p class="small">12 přidaných autorů</p>
  </div>
</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Profile"
}
</script>

<style scoped>
.avatar {
  width: 150px;

}


.title {
  font-size: 2em;

}


.points {
  color:     #929292;
  font-size: 1.2em;
}
</style>
