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
          <input type="email" placeholder="Your email….">
          <i name="fa fa-paper-plane"></i>
          <hr>
        </form>
      </div>
    </div>
    <img src="../assets/images/group-9.png"
      srcset="../assets/images/group-9@2x.png 2x,
        ../assets/images/group-9@3x.png 3x"
      class="Group-9">
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
footer .row .col-2{
  width: 18%
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
.signup, footer .row .col-3 form input{
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.39px;
  color: #9b9b9b;
}
footer .row .col-3 form input{
  background-color: #211f20;
  border: none;
}
footer .row .col-3 form hr{
  color: #211f20;
}
.Group-9{
  object-fit: contain;
  float: right;
  margin-right: 170px;
}
li a{
  text-decoration: none;
}
</style>