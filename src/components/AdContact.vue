<template>
  <div>
    <p class="contact-us">
      <span class="contact-us-directly">{{ contactMessage }} {{numbers}}</span>
      <span class="-local-time-12-00"> ( Local time {{time()}} )</span>
      <span class="lang">EN  <i name="fa fa-angle-down" ></i></span>
    </p>
    <hr/>
  </div>
</template>

<script>
export default {
  name: 'AdContact',
  data: () => {
    return {
      contactMessage: 'Contact us directly at',
      numbers: '01 33943  +234 807 340 4890',
    }
  },
  methods: {
    time: () => {
        let date = new Date();
        return `${(date.getHours() + '').length > 1 ? date.getHours() : `0${date.getHours()}`} : ${(date.getMinutes() + '').length > 1 ? date.getMinutes() : `0${date.getMinutes()}`}`;
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.lang{
  float: right;
}
div{
  margin-bottom: 10px;
}
.contact-us {
  height: 17px;
  font-family: OpenSans;
  font-size: 12px;
  font-weight: normal;
  letter-spacing: 0.5px;
  text-align: justify;
}
.contact-us-directly {
  width: 309px;
}
.-local-time-12-00 {
  width: 118px;
}
hr{
  size: 1;
  color: #e0e2e5;
  margin-top: -10px;
}

</style>