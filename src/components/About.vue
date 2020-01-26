<template>
  <div class="about">
    <div>
      <h1>about us</h1>
      <h3>A best place to enjoy your life</h3>
      <p>Transcorp Hilton Hotel is situated in the heart of Nigeria’s Federal Capital Territory, a 40-minute drive from the Nnamdi Azikiwe International Airport in Abuja. It is a 670–room, 5-star hotel that provides luxury accommodation, exotic cuisine, and fully equipped meeting rooms and to business travellers and tourists from all over the world.</p>
    </div>
    <img src="../assets/images/rectangle-7.png"
      srcset="../assets/images/rectangle-7@2x.png 2x,
              ../assets/images/rectangle-7@3x.png 3x"
      class="Rectangle-7">
    <div class="con-space">
      <a class="link">view more pictures</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.about{
  margin: 100px auto;
  text-align: center;
  width: 100%;
}
.about div{
  margin: 100px auto;
  width: 600px;
}
.about div h1{
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: bold;
  letter-spacing: 4.94px;
  color: #9b9b9b;
  text-transform: uppercase;
}
.about div h3{
  font-family: 'Georgia';
  font-size: 52px;
  font-weight: normal;
  letter-spacing: 3.06px;
  text-align: center;
  color: #000000;
}
.about div p{
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 2;
  letter-spacing: 0.82px;
  color: #9b9b9b;
}
.Rectangle-7 {
  height: 300px;
  object-fit: contain;
  border: solid 10px #ffffff;
}
.link{
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: bold;
  letter-spacing: 4.94px;
  text-align: justify;
  color: #9b9b9b;
  text-decoration: underline;
}
div.con-space{
  margin-top: 60px;
  margin-bottom: 100px;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .about div{
    width: 90%;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {

}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .about div{
    width: 80%;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .about div{
    width: 60%;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .about div{
    width: 50%;
  }
}
</style>