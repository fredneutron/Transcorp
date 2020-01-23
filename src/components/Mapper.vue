<template>
  <div class="gmap_canvas" :height="height">
    <iframe
    :width="width"
    :height="height"
    :src="src"
    frameborder="0"
    scrolling="no"
    marginheight="0"
    marginwidth="0"
    >
      <a href="https://www.maps.ie/coordinates.html">find my location</a>
    </iframe>
  </div>
</template>
<script>
export default {
  name: 'Mapper',
  props: {
    height: {
      type: String,
      default: '700px',
      required: false
    },
    width: {
      type: String,
      default: '100%',
      required: false,
    },
    src: {
      type: String,
      default: 'https://maps.google.com/maps?q=transcorp%20hotel%20abuja&t=&z=15&ie=UTF8&iwloc=&output=embed',
      required: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.gmap_canvas{
  overflow: hidden;
  background: none!important;
  width: 100%
}
</style>