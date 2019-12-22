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
        src: ''
      },
      {
        name: 'About Us',
        src: ''
      },
      {
        name: 'Our Rooms',
        src: ''
      },
      {
        name: `<img src='${require(`../assets/images/transcorp-1.png`)}' srcset='${require(`../assets/images/transcorp-1@2x.png`)} 2x, ${require(`../assets/images/transcorp-1@3x.png`)} 3x' class='transcorp1'>`,
        src: ''
      },
      {
        name: 'Reservation',
        src: ''
      },
      {
        name: 'Blog',
        src: ''
      },
      {
        name: 'Contact Us',
        src: ''
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
  width: 190px;
  height: 39px;
  -o-object-fit: contain;
     object-fit: contain;
}

</style>
