<template>
  <div class="luxury-in row">
    <div class="col-5">
      <p>DISCOVER OUR ROOMS</p>
      <h1>Luxury interior</h1>
      <div class="col-12" >
        <div class="row">
          <div class="col-6">
            <div
              class="row"
              v-for="(item, index) in rooms"
              :key="index"
              >
              <div class="col-4">
                <img :src="require(`../assets/images/${item.image.src}`)"
                  :srcset="`${require(`../assets/images/${item.image.srcset.x2}`)} 2x, ${require(`../assets/images/${item.image.srcset.x3}`)} 3x`"
                  class="Rectangle-9-Copy">
              </div>
              <div class="col-8">
                <h3>{{item.name}} Room</h3>
                <p>Starting from <span>${{item.price}}</span>/Night</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="col-7">
      <img src="../assets/images/rectangle-8-copy.png"
        srcset="../assets/images/rectangle-8-copy@2x.png 2x,
          ../assets/images/rectangle-8-copy@3x.png 3x"
        class="Rectangle-8-Copy">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Room',
  data: () => {
    return {
      rooms: [
        {
          name: 'Classic',
          price: 40.00,
          image: {
            src: 'rectangle-9-copy-2.png',
            srcset: {
              x2: 'rectangle-9-copy-2@2x.png',
              x3: 'rectangle-9-copy-2@3x.png'
            }
          }
        },
        {
          name: 'Classic',
          price: 40.00,
          image: {
            src: 'rectangle-9-copy-2.png',
            srcset: {
              x2: 'rectangle-9-copy-2@2x.png',
              x3: 'rectangle-9-copy-2@3x.png'
            }
          }
        },
        {
          name: 'Classic',
          price: 40.00,
          image: {
            src: 'rectangle-9-copy-2.png',
            srcset: {
              x2: 'rectangle-9-copy-2@2x.png',
              x3: 'rectangle-9-copy-2@3x.png'
            }
          }
        },
        {
          name: 'Deluxe',
          price: 65.99,
          image: {
            src: 'rectangle-9-copy-3.png',
            srcset: {
              x2: 'rectangle-9-copy-3@2x.png',
              x3: 'rectangle-9-copy-3@3x.png'
            }
          }
        },
        {
          name: 'Classic',
          price: 40.00,
          image: {
            src: 'rectangle-9-copy-2.png',
            srcset: {
              x2: 'rectangle-9-copy-2@2x.png',
              x3: 'rectangle-9-copy-2@3x.png'
            }
          }
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.luxury-in{
  background-color: #ffffff;
  padding: 0;
}
.luxury-in > .col-7{
  padding: 0;
}
.luxury-in > .col-7 > img{
  object-fit: contain;
  width: 100%;
}
.luxury-in > .col-5{
  padding: 50px 0;
  background-color: #ffffff;
  text-align: center;
}
.luxury-in > .col-5 > p{
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: bold;
  letter-spacing: 4.94px;
  color: #9b9b9b;
}
.luxury-in > .col-5 > h1{
  font-family: 'Georgia';
  font-size: 36px;
  font-weight: normal;
  letter-spacing: 2.12px;
  color: #000000;
}
.luxury-in > .col-5 > div.col-12{
  text-align: center;
  margin: 0 auto;
  left: 0;
  right: 0;
}
.luxury-in > .col-5 > div.col-12 > .row{
  padding: 0;
}
.luxury-in > .col-5 > div.col-12 > .row > .col-6{
  height: 250px;
  overflow-y: auto;
  overflow-x: hidden;
  text-align: center;
  flex: none;
}
.luxury-in > .col-5 > div.col-12 > .row > .col-6::-webkit-scrollbar{
  width: 3px;
  background-color: #F5F5F5;
  margin-right: 50px;
}
.luxury-in > .col-5 > div.col-12 > .row > .col-6::-webkit-scrollbar-thumb{
  background-color: #000000;
}
.luxury-in > .col-5 > div.col-12 > .row > .col-6::-webkit-scrollbar-track{
  background-color: #F5F5F5;
}

.luxury-in > .col-5 > div.col-12 > .row > .col-6 > .row:hover{
  background-color: #f5f5f5;
}
.luxury-in > .col-5 > div.col-12 > .row > .col-6 > .row > div.col-8 > h3{
  font-family: 'Georgia';
  font-size: 17px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 1px;
  text-align: justify;
  color: #000000;
  margin: 3px 0px;
}
.luxury-in > .col-5 > div.col-12 > .row > .col-6 > .row > div.col-8 > p{
  font-family: 'Georgia';
  font-size: 12px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.71px;
  text-align: justify;
  color: #b5b5b5;
  
}
.luxury-in > .col-5 > div.col-12 > .row > .col-6 > .row > div.col-8 > p > span{
  color: #000000;
}
.Rectangle-9-Copy{
  width: 120px;
  height: 80px;
  object-fit: contain;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .room{
    z-index: 2;
    margin-top: -220%;
    flex-direction: column;
  }
  .luxury-in > .col-5{
    width: 100%;
  }
  .luxury-in > .col-5 > div.col-12{
    width: 85%;
  }
  .luxury-in > .col-5 > div.col-12 > .row > .col-6{
    width: 100%;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {

}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .room{
    z-index: 2;
    margin-top: -970px;
    flex-direction: column;
  }
  .luxury-in > .col-5{
    width: 100%;
  }
  .luxury-in > .col-5 > div.col-12{
    width: 60%;
  }
  .luxury-in > .col-5 > div.col-12 > .row > .col-6{
    width: 100%;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .room{
    z-index: 2;
    margin-top: -1350px;
    flex-direction: row;
  }
  .luxury-in > .col-5{
    padding: 30px 0;
  }
  .luxury-in > .col-5 > div.col-12{
    width: 80%;
  }
  .luxury-in > .col-5 > div.col-12 > .row > .col-6{
    width: 100%;
    height: 200px;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .room{
    z-index: 2;
    margin-top: -1700px;
    flex-direction: row;
  }
  .luxury-in > .col-5{
    padding: 50px 0;
  }
  .luxury-in > .col-5 > div.col-12 > .row > .col-6{
    height: 250px;
  }
}
</style>