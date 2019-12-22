<template>
  <iframe :width="width" :height="height" src="https://maps.google.com/maps?width=100%&amp;height=600&amp;hl=en&amp;q=1%20Aguiyi%20Ironsi%20St%20Maitama%20900001%20Abuja%20Nigeria+(Transcorp)&amp;ie=UTF8&amp;t=&amp;z=14&amp;iwloc=B&amp;output=embed" frameborder="0" scrolling="no" marginheight="0" marginwidth="0">
    <a href="https://www.maps.ie/coordinates.html">find my location</a>
  </iframe>
</template>
<script>
export default {
  name: 'Map',
  props: {
    height: {
      type: Number,
      default: 600,
      required: false
    },
    width: {
      type: String,
      default: '100%',
      required: false,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>