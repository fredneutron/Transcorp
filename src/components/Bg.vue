<template>
  <div>
    <img src="../assets/images/rectangle-11.png"
      srcset="../assets/images/rectangle-11@2x.png 2x"
      class="Rectangle-11">
    <room class="room" id="rooms"/>
    <testimonial />
    <blog id="blog" />
  </div>
</template>

<script>
export default {
  name: 'Bg',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.Rectangle-11 {
  margin-top: 50px;
  padding: 0;
  width: 100%;
  object-fit: contain;
  z-index: 1;
}
.room{
  z-index: 2;
  margin-top: -1800px;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .bg{
    margin-top: 0px;
  }
}
</style>