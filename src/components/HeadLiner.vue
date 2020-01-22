<template>
  <div class="headliner">
    <p>welcome to</p>
    <h1>Transcorp Hotel</h1>
    <p class="motto">A place to experience and enjoy the life</p>
    <img src="../assets/images/ic-play-circle-outline.png"
      srcset="../assets/images/ic-play-circle-outline@2x.png 2x,
              ../assets/images/ic-play-circle-outline@3x.png 3x"
      class="ic_play_circle_outline">
    <header-line class="-head"/>
  </div>
</template>

<script>
export default {
  name: 'HeadLiner',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.headliner{
  height: 607px;
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0.7), rgba(67, 67, 67, 0.2)), url('../assets/images/rectangle-3.png');
  background-size: cover;
  background-repeat: no-repeat;
  margin-bottom: 100px;
}
.headliner {
    color: #ffffff;
    text-align: center;
    padding-top: 150px;
}
.headliner > :first-child{
  height: 18px;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: bold;
  letter-spacing: 4.94px;
  text-transform: uppercase;
}
.headliner > h1 {
  font-family: 'Georgia';
  font-size: 52px;
  font-weight: normal;
  letter-spacing: 3.06px;
}
.motto{
  font-family: OpenSans;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 0.82px;
}
.ic_play_circle_outline{
  width: 50px;
  height: 50px;
  object-fit: contain;
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (max-width: 600px) {
  .-head{
    margin-top: 300px;
    width: 100%;
  }
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .-head{
    margin-top: 300px;
    width: 95%;
  }
  button.promo-btn{
    width: 120px;
    height: 40px;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  button.promo-btn{
    width: 150px;
    height: 45px;
  }
  .-head{
    margin-top: 300px;
    width: 80%;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .-head{
    margin-top: 300px;
    width: 65%;
  }
}
</style>