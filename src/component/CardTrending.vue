<template>
  <div class="container">
    <p class="sub">Trending</p>
    <div class="row mb-3">
      <h4 class="col-sm-10">Trending Destinations</h4>
      <a class="col-sm-2">View All</a>
    </div>
    <section class="main">
      <div class="card">
        <div class="top-card mt-3 ml-3">
          <p class="ml-3 mt-1"><b>15</b> Airlines</p>
        </div>
        <div class="row city">
          <div class="col-sm-8">
            <p>Tokyo,</p>
            <h4 h4>Japan</h4>
          </div>
          <div class="col-sm-2 btn-right">
            <img src="../assets/img/btnback.png">
          </div>
        </div>
      </div>
      <div class="card">
        <div class="top-card mt-3 ml-3">
          <p class="ml-3 mt-1"><b>15</b> Airlines</p>
        </div>
        <div class="row city">
          <div class="col-sm-8">
            <p>Tokyo,</p>
            <h4 h4>Japan</h4>
          </div>
          <div class="col-sm-2 btn-right">
            <img src="../assets/img/btnback.png">
          </div>
        </div>
      </div>
      <div class="card">
        <div class="top-card mt-3 ml-3">
          <p class="ml-3 mt-1"><b>15</b> Airlines</p>
        </div>
        <div class="row city">
          <div class="col-sm-8">
            <p>Tokyo,</p>
            <h4 h4>Japan</h4>
          </div>
          <div class="col-sm-2 btn-right">
            <img src="../assets/img/btnback.png">
          </div>
        </div>
      </div>
      <div class="card">
        <div class="top-card mt-3 ml-3">
          <p class="ml-3 mt-1"><b>15</b> Airlines</p>
        </div>
        <div class="row city">
          <div class="col-sm-8">
            <p>Tokyo,</p>
            <h4>Japan</h4>
          </div>
          <div class="col-sm-2 btn-right">
            <img src="../assets/img/btnback.png">
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
// import { mapGetters, mapActions } from 'vuex'

export default {
  name: 'CardTrending'
  // computed: {
  //   ...mapGetters({
  //     getLocation: 'location/getLocation'
  //   })
  // },
  // method: {
  //   ...mapActions({
  //     getCity: 'location/getLocation'
  //   })
  // },
  // mounted () {
  //   this.getCity()
  // }
}

</script>
<style scoped>
.container {
  display: grid;
  margin-bottom: 5%;
}
.main {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 10px;
}
.card {
  background-image: url(../assets/img/trending1.png);
  background-size: cover;
  background-repeat: no-repeat;
  height: 260px;
  width: 200px;
  border-radius: 20px;
  color: #fff;
  position: relative;
}
.card:hover {
  box-shadow: 20px -20px rgba(115, 115, 115, 0.65),
              40px -40px rgba(196, 196, 196, 0.65);
  margin: 30px 0 -30px -20px;
  transition: all .4s ease;
}
.top-card {
  background-color: rgba(255, 255, 255, 0.41);
  border-radius: 20px;
  font-size: 12px;
  width: 88px;
  height: 28px;
}
.card::after {
  content: "";
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
  position: absolute;
  bottom: 0;
  border-radius: 20px;
}
.city {
  z-index: 1;
  margin: 60% 0 0 10%;
}
.btn-right {
  margin-top: 20%;
  background: rgba(255, 255, 255, 0.17);
  border-radius: 20px;
  height: 29px;
  width: 29px;
}
.btn-right img {
  margin-left: -7px;
}
.sub {
  color: #2395ff;
  letter-spacing: 0.3em;
}
@media (max-width: 576px) {
  .main {
    margin: 0 auto;
  }
  .btn-right {
    margin: -20% 0 0 60%;
  }
}
</style>
