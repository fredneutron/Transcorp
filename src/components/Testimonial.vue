<template>
  <div class="row t">
    <div class="testimonials">
      <p class="testimonials-head">TESTIMONIALS</p>
        <div
          class="slide"
          v-for="(item, index) in testimonies"
            :key="index"
        >
          <h1>What guests Say</h1>
          <blockquote>
            <p class="quote">“{{ item.message }}”</p>
          </blockquote>
          <img
            :src="`${require(`../assets/images/${item.image.src}`)}`"
            :srcset ="`${require(`../assets/images/${item.image.srcset.x2}`)} 2x,${require(`../assets/images/${item.image.srcset.x3}`)} 3x`"
            class="author-image">
          <h2 class="author-name">{{ item.name }}</h2>
        </div>
        <div class="dot-horizon" style="text-align:center">
          <span
            v-for="(item, index) in testimonies"
            :key="index"
            @click="viewSlide(index)"
            class="dot"></span>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Testimonial',
  data: () => {
    return {
      testimonies: [
        {
          name: 'FARAH WILIAMS',
          image: {
            src: 'oval.png',
            srcset: {
              x2: 'oval@2x.png',
              x3: 'oval@3x.png'
            }
          },
          message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo urna id neque finibus, ac sollicitudin arcu tempus. In hac habitasse platea dictumst'
        },
        {
          name: 'FARAH WILIAMS',
          image: {
            src: 'oval.png',
            srcset: {
              x2: 'oval@2x.png',
              x3: 'oval@3x.png'
            }
          },
          message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo urna id neque finibus, ac sollicitudin arcu tempus. In hac habitasse platea dictumst'
        },
        {
          name: 'SARAH WILIAMS',
          image: {
            src: 'oval.png',
            srcset: {
              x2: 'oval@2x.png',
              x3: 'oval@3x.png'
            }
          },
          message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo urna id neque finibus, ac sollicitudin arcu tempus. In hac habitasse platea dictumst'
        },
        {
          name: 'Ishola WILIAMS',
          image: {
            src: 'oval.png',
            srcset: {
              x2: 'oval@2x.png',
              x3: 'oval@3x.png'
            }
          },
          message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo urna id neque finibus, ac sollicitudin arcu tempus. In hac habitasse platea dictumst'
        },
        {
          name: 'Pherrel WILIAMS',
          image: {
            src: 'oval.png',
            srcset: {
              x2: 'oval@2x.png',
              x3: 'oval@3x.png'
            }
          },
          message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo urna id neque finibus, ac sollicitudin arcu tempus. In hac habitasse platea dictumst'
        },
      ],
      currentSlide: 0,
    }
  },
  methods: {
    viewSlide(index) {
      let stage = document.querySelectorAll('.slide');
      let dot = document.querySelectorAll('.dot');
      stage.forEach((e, i) => i === index ? e.style.display = 'block' : e.style.display = 'none');
      dot.forEach((e, i) => i === index ? e.style.backgroundColor = '#ff7200' : e.style.backgroundColor = '#fff');
    },
    changeSlide() {
      // display current slide only 
      this.viewSlide(this.currentSlide);
      // set conditional rule for time func
      (this.currentSlide < (this.testimonies.length-1)) ? this.currentSlide+= 1 : this.currentSlide = 0;
    },
  },
  created() {
    window.onload = this.changeSlide(); 
    setInterval(() => this.changeSlide(), 5000);
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.t{
  text-align: center;
  margin: 10px auto;
  width: 70%;
  left: 0;
  right: 0;
}
.testimonials{
  margin-top: 100px;
  background-color: #ffffff;
  padding: 50px 5px 5px 5px;
}
.testimonials-head{
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 4.94px;
  color: #9b9b9b;
}
.testimonials div.slide{
  display: none;
}
.testimonials div h1{
  font-family: 'Georgia';
  font-size: 36px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 2.12px;
  color: #000000;
}
.testimonials div blockquote{
  width: 72%;
  font-family: 'Georgia';
  font-size: 24px;
  font-weight: normal;
  font-stretch: normal;
  font-style: italic;
  line-height: 1.46;
  letter-spacing: 1.41px;
  text-align: center;
  color: #000000;
  margin: 20px auto;
  left: 0;
  right: 0;
}
.author-name{
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 17px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 1px;
  text-align: center;
  text-transform: uppercase;
  color: #000000;
}
.author-image{
  text-align: center;
  width: 100px;
  height: 100px;
  object-fit: contain;
  margin: 20px auto;
  left: 0;
  right: 0;
}
.dot-horizon{
  margin: 20px 0px;
}
.dot {
  cursor: pointer;
  height: 8px;
  width: 8px;
  margin: 0 2px;
  background-color: #fff;
  border-radius: 50%;
  border: solid 1px #d8d8d8;
  display: inline-block;
  transition: background-color 0.6s ease;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .t{
    width: 100%;
  }
  .testimonials div blockquote{
    width: 80%;
  }
}
</style>