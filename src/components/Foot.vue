<template>
  <footer>
    <div class="row">
      <div class="col-2"></div>
      <div
        class="col-2"
        v-for="(item, index) in footer"
        :key="index"
      >
        <ul>
          <li
            v-for="(e, i) in item"
            :key="i"
          ><a :href="e.link">{{ e.name }}</a></li>
        </ul>
      </div>
      <div class="col-3">
        <p class="signup">Sign up to get our newsletter</p>
        <form>
          <div>
            <input type="email" placeholder="Your email….">
            <i name="fa fa-paper-plane"></i>
            <hr>
          </div>
        </form>
      </div>
    </div>
    <div class="social">
      <a href="#"><img src="../assets/images/fill-3.png"
      srcset="../assets/images/fill-3@2x.png 2x,
        ../assets/images/fill-3@3x.png 3x"
      class="Group-9"></a>
      <i name=""></i>
      <a href="#"><img src="../assets/images/fill-1.png"
      srcset="../assets/images/fill-1@2x.png 2x,
        ../assets/images/fill-1@3x.png 3x"
      class="Group-9"></a>
      <i name=""></i>
      <a href="#"><img src="../assets/images/group-7.png"
      srcset="../assets/images/group-7@2x.png 2x,
        ../assets/images/group-7@3x.png 3x"
      class="Group-9"></a>
      <i name=""></i>
      <a href="#"><img src="../assets/images/fill-33.png"
      srcset="../assets/images/fill-33@2x.png 2x,
        ../assets/images/fill-33@3x.png 3x"
      class="Group-9"></a>
      <a href="#"><img src="../assets/images/fill-23.png"
      srcset="../assets/images/fill-23@2x.png 2x,
        ../assets/images/fill-23@3x.png 3x"
      class="Group-9"></a>
      <i name=""></i>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Foot',
  data: () => {
    return {
      footer: [
        [
          {
            name: 'Site Map',
            link: ''
          },
          {
            name: 'Terms and Condition',
            link: ''
          },
          {
            name: 'Privacy Policy',
            link: ''
          },
          {
            name: 'Help',
            link: ''
          },
          {
            name: 'Affiliate',
            link: ''
          }
        ],
        [
          {
            name: 'Our Location',
            link: ''
          },
          {
            name: 'Career',
            link: ''
          },
          {
            name: 'About',
            link: ''
          },
          {
            name: 'Contact',
            link: ''
          }
        ],
        [
          {
            name: 'FAQs',
            link: ''
          },
          {
            name: 'Blog',
            link: ''
          },
          {
            name: 'Car Blog',
            link: ''
          },
          {
            name: 'Location',
            link: ''
          },
          {
            name: 'Press',
            link: ''
          }
        ]
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
footer{
  height: 343px;
  border: solid 0.1px #979797;
  background-color: #211f20;
  text-align: justify;
}
footer .row{
  margin-top: 80px;
}
footer div.row div.col-2 ul li{
  height: 18px;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.39px;
  color: #9b9b9b;
  list-style-type: none;
  padding-bottom: 5px;
  list-style-type: none;
}
footer div.row div.col-2 ul li a{
  color: #9b9b9b;
}
footer .row .col-3 form div{
  width: 190px;
}
.signup, footer .row .col-3 form div input{
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.39px;
  color: #9b9b9b;
  
}
footer .row .col-3 form div input{
  background-color: #211f20;
  border: none;
  width: 190px;
  outline: none;
}
footer .row .col-3 form div hr{
  color: #211f20;
}
.Group-9{
  object-fit: contain;
  padding: 0px 10px;
}
.social{
  float: right;
  margin-right: 130px;
}
li a{
  text-decoration: none;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  footer{
    height: 700px;
  }
  footer > .row{
    flex-direction: column;
    flex-wrap: wrap;
  }
  footer > .row >.col-2{
    width: 100%
  }
  footer > .row >.col-3, .social{
    margin-left: 10.7%;
  }
  .social{
    float: left;
    width: 100%;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
  
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  footer{
    height: 700px;
  }
  footer > .row{
    flex-direction: column;
    flex-wrap: wrap;
  }
  footer > .row >.col-2{
    width: 25%
  }
  footer > .row >.col-3{
    margin-left: 5%;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  footer{
    height: 343px;
  }
  footer > .row{
    flex-direction: row;
    flex-wrap: wrap;
  }
  footer > .row >.col-2{
    width: 20%
  }
  footer > .row >.col-3{
    margin-left: 0%;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  footer >.row >.col-2{
    width: 18%
  }
}
</style>