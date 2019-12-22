<template>
  <div class="connect">
    <div class="row">
      <map width="58%" class="col-7" />
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

</style>