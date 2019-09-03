<template>
  <div class="blog">
    <h1>Latest from our Blog</h1>
    <div class="row">
      <div
        class="col-7"
        v-for="(item, index) in articles"
        :key="index"
      >
        <div class="card">
          <div class="col">
            <img
              :src="`${require(`../assets/images/${item.image.src}`)}`"
              :srcset ="`${require(`../assets/images/${item.image.srcset.x2}`)} 2x,${require(`../assets/images/${item.image.srcset.x3}`)} 3x`"
              class="Rectangle-4-Copy-7">
            <div class="blog-card">
              <span>{{ reformat(item.date)}}</span>
              <h3>{{ item.title }}</h3>
              <a :href="item.link"><span>Continue</span><i name="fa fa-long-arrow-alt-right"></i></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Blog',
  data: () => {
    return {
      articles: [
        {
          title: 'Five reasons to  stay at the beautiful Transcorp Hotel',
          date: '04/10/2018',
          image: {
            src: 'rectangle-4-copy-7.png',
            srcset: {
              x2: 'rectangle-4-copy-7@2x.png',
              x3: 'rectangle-4-copy-7@3x.png'
            }
          },
          link: ''
        },
        {
          title: 'Five reasons to  stay at the beautiful Transcorp Hotel',
          date: '04/10/2018',
          image: {
            src: 'rectangle-4-copy-7.png',
            srcset: {
              x2: 'rectangle-4-copy-7@2x.png',
              x3: 'rectangle-4-copy-7@3x.png'
            }
          },
          link: ''
        },
        {
          title: 'Five reasons to  stay at the beautiful Transcorp Hotel',
          date: '04/10/2018',
          image: {
            src: 'rectangle-4-copy-7.png',
            srcset: {
              x2: 'rectangle-4-copy-7@2x.png',
              x3: 'rectangle-4-copy-7@3x.png'
            }
          },
          link: ''
        }
      ],
      monthToString: [ 'January', 'February', 'March', 'April', 'May', 'June', 'July', 'July', 'August', 'September', 'October', 'November', 'December']
    }
  },
  methods: {
    reformat(date) {
      let n = new Date(date);
      let month = n.getMonth();
      let day = n.getDate();
      let year = n.getFullYear();
      return `${this.monthToString[month]} ${day == 1 ? `${day}st` : day == 2 ? `${day}nd` : day == 3 ? `${day}rd` : `${day}th`}, ${year}`;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.blog{
  margin: 50px auto;
  width: 70%;
}
.blog .row .col-7{
  margin: 0px 5px
}
.blog-card{
  text-align: left;
  padding: 5px 20px;
  background-color: #ffffff;
  margin-top: -4px;
}
.blog h1{
  font-family: 'Georgia';
  font-size: 36px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 2.12px;
  text-align: center;
  color: #4a4a4a;
}
.blog-card span{
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.82px;
  text-align: center;
  color: #9b9b9b;
}
.blog-card h3{
  font-family: 'Georgia';
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: 0.82px;
  color: #000000;
}
.blog-card a{
  text-decoration: none;
}
.Rectangle-4-Copy-7{
  width: 100%;
  object-fit: contain;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .blog > .row{
    flex-direction: column;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {

}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .blog > .row{
    flex-direction: column;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .blog > .row{
    flex-direction: row;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  
}
</style>