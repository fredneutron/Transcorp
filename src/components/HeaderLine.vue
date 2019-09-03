<template>
    <div class="card header-card">
        <div class="card-body">
            <div class="card-col">
                <div>
                    <p class="check-in">check-in</p>
                    <p>
                        <span class="day">24</span>
                        <span class="month">/june </span>
                        <span class="icon"><i class="fa fa-angle-down"></i></span>
                    </p>
                </div>
            </div>
            <div class="card-col">
                <div>
                    <p class="check-out">check-out</p>
                    <p>
                        <span class="day">24</span>
                        <span class="month">/june</span>
                        <span class="icon"><i class="fa fa-angle-down"></i></span>
                    </p>
                </div>
            </div>
            <div class="card-col">
                <div>
                    <p class="guest">guests</p>
                    <p>
                        <span class="day">24</span>
                        <span class="icon"><i class="fa fa-angle-down"></i></span>
                    </p>
                </div>
            </div>
            <div class="card-col">
                <p class="promo">Have a promotional code ?</p>
                <button class="promo-btn">check availablity</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HeaderLine',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card{
    margin: 0 auto;
}
.header-card{
  background-color: #ffffff;
  margin-top: 302px;
}
.card:hover {
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}
.card-body{
  padding: 0px 0px;
  display: flex;
  flex-direction: row;
  background-color: #ffffff;
}
.card-col{
  flex: 175;
}
.card-col div{
    border-right: 2px solid #e0e2e5;
    margin: 10px 0;
    height: 100px;
}
.card-body div.card-col:last-child{
  background-color: #053b58;
  text-align: center;
}
.card-body > div:last-child > p{
  font-family: 'Source Sans Pro', sans-serif;
  text-align: center;
  color: #ffffff;
}
.card-body > div:last-child > p, .check-in, .check-out, .guest, span.month{
    font-size: 14px;
    font-weight: normal;
    letter-spacing: 0.58px;
}
.check-in, .check-out, .guest, span.month{
    font-family: OpenSans;
}
.check-in, .check-out, .guest{
    text-align: justify;
    color: #9b9b9b;
}
.check-in, .check-out{
    margin-left: 50px;
}
.guest{
    margin-left: 70px;
}
.check-in, .check-out, .guest, span.day, span.month, .card-col > button{
    text-transform: uppercase;
}
span.day{
  font-family: BodoniSvtyTwoITCTT;
  font-size: 48px;
  font-weight: normal;
  letter-spacing: 2px;
}
span.day, span.month{
  text-align: justify;
  color: #000000;
}
.card-col > button{
  width: 170px;
  height: 48px;
  background-color: #ff7200;
  border: none;
  color: #ffffff;
}
.icon{
    text-align: right;
}
</style>