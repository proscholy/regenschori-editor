<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
      <a class="navbar-brand"
         href="#">REGENSCHORI - rozhraní pro doplňování</a>
      <button class="navbar-toggler"
              type="button"
              data-toggle="collapse"
              data-target="#navbarNav"
              aria-controls="navbarNav"
              aria-expanded="false"
              aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse"
           id="navbarNav">
        <ul class="navbar-nav">
        </ul>
      </div>
    </nav>

    <div class="container-fluid">
      <Nuxt/>
    </div>
  </div>
</template>

<style>

@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@200;400;600&display=swap');


body {
  font-family: "Nunito", Arial, sans-serif;

  margin-top: 95px;
}


.navbar {
  margin-bottom: 20px;

  /*padding: .5rem ;*/
  z-index: 200;
  background-color: #112362;
  min-height: 66px;
  font-family: Nunito,sans-serif;
}


.material-shadow {
  box-shadow: 0 2px 2px 0 rgba(0, 0, 0, .14), 0 3px 1px -2px rgba(0, 0, 0, .2), 0 1px 5px 0 rgba(0, 0, 0, .12);
  border:     none !important;
}

</style>
