<template>
  <div class="connect">
    <div class="row">
      <mapper width="100%" height="700px" class="col-7" />
      <connect :state="state" :address="address" :email="email" :phoneNumber="phoneNumber" class="col-5" />
    </div>
  </div>
</template>
<script>
export default {
  name: 'Contact',
  data: () => {
    return {
      address: 'Address: 1 Aguiyi Ironsi St, Abuja 900001, Nigeria',
      email: 'info@transcorphotelsplc.com',
      state: 'Abuja',
      phoneNumber: 7080603000,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.connect{
  z-index: 1;
  width: 100%;
  text-align: justify;
 }
 .connect .row{
   width: 100%;
   padding: 0;
 }
 .connect .row .col-7{
   padding: 0;
 }
 .connect .row .col-5{
   padding-left: 80px;
   padding-top: 20px;
   background-color: #ffffff;
 }
 /* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .connect > .row{
    flex-direction: column-reverse;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {

}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .connect > .row{
    flex-direction: column-reverse;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .connect > .row{
    flex-direction: row;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .connect{
    margin-top: -100px;
  }
  .connect > .row{
    flex-direction: row;
  }
}
</style>