<template>
  <div>
  <!-- <b-navbar toggleable="lg" type="faded" variant="light" class="justify-content-center"> -->
    <!-- <b-navbar-brand href="/" class="text-center">Shivam Auto Parts</b-navbar-brand> -->

     <!-- <b-collapse id="nav-collapse" is-nav>
       <b-navbar-nav>
          <b-nav-item href="#contact">Contact</b-nav-item>
        </b-navbar-nav>
     </b-collapse> -->
    <!--  <b-navbar-nav class="ml-auto">
        <b-navbar-nav>
          <b-nav-item href="#contact">Contact</b-nav-item>
        </b-navbar-nav>
      </b-navbar-nav>
    </b-collapse> -->
  <!-- </b-navbar> -->
  <!-- <div class="text-center text-bold div-height">
    <div class="div-padding">
      <a href="/" class="a-decorate"><span>Shivam Auto Parts</span></a>
    </div>
    
  </div> -->
  <nav class="nav sticky-top justify-content-center m-3">
    <li class="nav-item">
      <a class="a-decorate " href="/">SHIVAM AUTO SPARES</a>
    </li>
  </nav>
  <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide
        caption="Break Shoe"
        text="Write something about this picture"
      >
        <template #img>
          <img
            class="d-block img-fluid w-100 img-class"
            src="../assets/pair.png"
            alt="image slot"
          >
        </template>
      </b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100 img-class"
            src="../assets/image2.jpg"
            alt="image slot"
          >
        </template>
      </b-carousel-slide>
    </b-carousel>
  </div>
  <div id="contact" class="row m-5">
    <div class="col-6 text-decorate">Shivam Auto Spares <br/> 
                       Manufacturer and Traders of two wheelers auto spares products <br/>
                       Deals in all types of clutch plates, brake shoes, gaskets and 100cc spares of two wheelers
    </div>
    <div class="col-2"></div>
    <div class="col-4"><b>Sales office:</b> 1495/25, Naiwala, Karol Bagh, New Delhi-110005 <br/>
                       <b>Email:</b> sarthakaggarw254@gmail.com <br/>
                       <b>Mobile:</b>
                       <div>
                         <ul style="list-style: none;">
                                <li> (+91) 9811895038 </li>
                                <li> (+91) 9891602346 </li>
                                <li> (+91) 7011187254 </li>
                               </ul> 

                       </div>
                       
    </div>
  </div>
</div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';

export default {
  name: 'Home',
  components: {
    Carousel,
    Slide
  },
  data() {
      return {
        slide: 0,
        sliding: null
      }
  },
    methods: {
      onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.img-class {
  width: 1024px;
  height: 800px;

}
.div-height {
  height: 100px;
}
.div-padding {
  margin-top: 50px;
}
.a-decorate {
  color: inherit;
  font-size: 30px;
}
.text-decorate {
  font-size: 20px;
}
</style>
