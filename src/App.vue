<template>
  <div id="app">
    <side-bar :toggle="toggle" :url="url" v-if="isSideBarActive === true" />
    <nav-bar class="nav" :toggle="toggle" :url="url" />
    <head-liner class="header" />
    <about id="about" />
    <bg class="bg" />
    <contact id="contact" />
    <foot />
  </div>
</template>

<script>

export default {
  name: 'app',
  data: () => {
    return {
      isSideBarActive: false,
      url: [
        {
        name: 'Home',
        src: '/.'
      },
      {
        name: 'About Us',
        src: '#about'
      },
      {
        name: 'Our Rooms',
        src: '#rooms'
      },
      {
        name: `<img src='${require(`./assets/images/transcorp-1.png`)}' srcset='${require(`./assets/images/transcorp-1@2x.png`)} 2x, ${require(`./assets/images/transcorp-1@3x.png`)} 3x' class='transcorp1'>`,
        src: '/.'
      },
      {
        name: 'Reservation',
        src: '#reserve'
      },
      {
        name: 'Blog',
        src: '#blog'
      },
      {
        name: 'Contact Us',
        src: '#contact'
      }]
    }
  },
  methods: {
    toggle() {
      this.isSideBarActive === true
        ? this.isSideBarActive = false
        : this.isSideBarActive = true;
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro&display=swap');
@font-face {
  font-family: 'Georgia';
  font-style: normal;
  font-weight: normal;
  src: local('Georgia Regular'), url('assets/fonts/georgia.woff') format('woff');
}
#app {
  margin-top: 0px;
  width: 100%;
}
div.nav{
  margin: 0px auto;
  position: absolute;
  left: 0;
  right: 0;
  position: relative;
  z-index: 1;
}
.toggle{
  border: 0px;
  background: none;
}
div.header{
  margin-top: 0px;
  z-index: 2;
}
.card{
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
}
.about{
  position: relative;
  z-index: 3;
}
.row{
  width: 100%;
  display: flex;
  flex-direction: row;
  padding: 5px 2px;
}
.col-1{
  flex: 8.33;
  display: flex;
  flex-direction: column;
  padding: 5px 4px;
}
.col-2{
  flex: 16.67;
  display: flex;
  flex-direction: column;
  padding: 5px 4px;
}
.col-3{
  flex: 25;
  display: flex;
  flex-direction: column;
  padding: 5px 4px;
}
.col-4{
  flex: 33.3;
  display: flex;
  flex-direction: column;
  padding: 5px 4px;
}
.col-5{
  flex: 41.7;
  display: flex;
  flex-direction: column;
  padding: 5px 4px;
}
.col-7{
  flex: 58.3;
  display: flex;
  flex-direction: column;
  padding: 5px 4px;
}
.col-8{
  flex: 66.7;
  display: flex;
  flex-direction: column;
  padding: 5px 4px;
}
.col-12{
  flex: 100%;
  display: flex;
  flex-direction: column;
  padding: 5px 4px;
  background: #ffffff;
}
.bg{
  margin-top: -380px;
  z-index: 2;
  margin-bottom: 122px;
}
footer{
  position: relative;
  z-index: 3;
}
</style>
