<template>
  <div class="nav">
    <ad-contact class="contact" />
    <div class="navbar">
      <nav>
        <ul>
          <li
            v-for="(item, index) in url"
            :key="index"
          ><a :href="item.src" v-html="item.name"></a></li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>

export default {
  name: 'NavBar',
  data: () => {
    return {
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
        name: `<img src='${require(`../assets/images/transcorp-1.png`)}' srcset='${require(`../assets/images/transcorp-1@2x.png`)} 2x, ${require(`../assets/images/transcorp-1@3x.png`)} 3x' class='transcorp1'>`,
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
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div.navbar{
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  -webkit-box-pack: center;
      -ms-flex-pack: center;
          justify-content: center;
  width: 100%;
  padding: 30px 0;
}
nav ul {
  margin: 20px 0px;
  padding: 0;
  list-style-type: none;
}
nav ul li{
  float: left;
  height: 18px;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: normal;
  letter-spacing: 0.58px;
  text-align: justify;
  color: #526173;
  padding: 15px 8px;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
}
nav ul li:nth-child(4){
  padding: 0 !important;
}
nav ul li a{
  display: block;
  text-decoration: none;
  color: #526173
}
.transcorp1{
  -o-object-fit: contain;
     object-fit: contain;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .contact{
    width: 95%;
    margin: 0px auto;
  }
  .nav{
    width: 100%;
  }
  .nav ul li{
    padding: 7px 4px;
  }
  .transcorp1{
    width: 50px !important;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {

}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .contact{
    width: 90%;
    margin: 0px auto;
  }
  .nav{
    width: 90%;
  }
  .nav ul li{
    padding: 10px 7px;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .contact{
    width: 80%;
    margin: 0px auto;
  }
  .nav{
    width: 80%;
  }
  .transcorp1{
    width: 150px;
    height:  39px;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .nav{
    width: 60%;
  }
  .transcorp1{
    width: 190px;
    height:  39px;
  }
}
</style>