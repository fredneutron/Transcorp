<template>
  <div class="sidebar">
    <button v-on:click="toggle"><font-awesome-icon icon="times" /></button>
    <ul>
      <li
        v-for="(item, index) in url"
        :key="index"
        v-on:click="toggle"
      ><a :href="item.src" v-html="item.name"></a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'SideBar',
  props: {
    toggle: {
      type: Function,
      required: true
    },
    url: {
      type: Array,
      required: true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sidebar{
  width: 95.6%;
  background-color: #526173;
  color: #ffffff;
  float: right;
  position: absolute;
  z-index: 99;
  height: 200%;
}
.sidebar > button{
  padding: 1%;
  float: right;
  margin-right: 10%; 
  margin-top: 2%;
  background: none;
  border: none;
}
.sidebar > button > .fa-times{
  font-size: 250%;
}
.sidebar > ul {
  list-style: none;
  padding-left: 40%;
  padding-top: 40px;
}
.sidebar > ul > li{
   padding: 5px 0px;
   border-bottom: 0.5px solid #526197;
}
.sidebar > ul > li > a{
  text-decoration: none;
  color: inherit;
}
.sidebar > ul > li:nth-child(4){
  display: none !important;
}
</style>