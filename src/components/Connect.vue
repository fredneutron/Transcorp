<template>
  <div>
    <h3 class="DISCOVER-OUR-ROOMS">DISCOVER OUR ROOMS</h3>
    <h1 class="Luxury-interior">Luxury interior</h1>
    <h3 class="state"><span class="Abuja">{{ state }},</span> <span class="Nigeria">Nigeria</span></h3>
    <p class="Address-1-Aguiyi-Ir">{{ address }}<br> Email: {{ email }}</p>
    <p class="Call-directly">Call directly;</p>
    <h1 class="phone">+234 {{ showNumber(phoneNumber) }}</h1>
  </div>
</template>
<script>
export default {
  name: 'Connect',
  props: {
    address: {
      type: String,
      required: true
    },
    email: {
      type: String,
      required: true
    },
    phoneNumber: {
      type: Number,
      default: 7080603000,
      required: true,
      validator: (number) => (number.length > 9)
    },
    state: {
      type: String,
      required: true
    }
  },
  methods: {
    showNumber(number) {
      // create a function to restructure
      const structure = (value) => `${value.substr(0, 3)} ${value.substr(3, 3)} ${value.substr(6)}`;
      // return structured value
      return number.length === 10
        ? structure(number+'')
        : structure(number+"".substr(1));
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
 .DISCOVER-OUR-ROOMS {
  margin-top: 60px;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 4.94px;
  text-align: justify;
  color: #9b9b9b;
}
.Luxury-interior {
  height: 41px;
  font-family: 'Georgia';
  font-size: 36px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 2.12px;
  color: #000000;
}
.state{
  margin-top: 64px;
}
.Abuja {
  height: 27px;
  font-family: 'Georgia';
  font-size: 24px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 1.41px;
  color: #000000;
}
.Nigeria {
  height: 27px;
  font-family: 'Georgia';
  font-size: 24px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 1.41px;
  color: #d8d8d8;
}
.Address-1-Aguiyi-Ir {
  height: 60px;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 2.14;
  letter-spacing: 0.82px;
  color: #9b9b9b;
}
.Call-directly {
  margin-top: 64px;
  height: 30px;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 2.14;
  letter-spacing: 0.82px;
  color: #9b9b9b;
}
.phone{
  height: 55px;
  font-family: 'Georgia';
  font-size: 36px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 2.12px;
  color: #000000;
}
</style>