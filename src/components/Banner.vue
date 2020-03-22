<template>
 <carousel :per-page="1" :mouse-drag="false" 
  :autoplay="false" :autoplayTimeout="3000" :loop="true" :navigationEnabled="true" 
  :paginationEnabled="false">
    <slide style="background-image: url(/media/slider/slide1.jpg)">
      <div class="slide-content">
        <div class="caption">Steel<br>Cylinders.</div>
        <button class="btn btn-success btn-rounded btn-lg">Production</button>
      </div>
    </slide>
    <slide style="background-image: url(/media/slider/slide2.jpg)">
    <div class="slide-content">
      <div class="caption">With high<br>Pressure.</div>
      <button class="btn btn-success btn-rounded btn-lg">Quality Standards</button>
    </div>
    </slide>
    <slide style="background-image: url(/media/slider/slide3.jpg)">
    <div class="slide-content">
      <div class="caption">Because<br>We can.</div>
      <button class="btn btn-success btn-rounded btn-lg">Home</button>
    </div>
    </slide>
    <slide style="background-image: url(/media/slider/slide4.jpg)">
      <div class="slide-content">
        <div class="caption">Seamless<br>Safe.</div>
        <button class="btn btn-success btn-rounded btn-lg">Company</button>
      </div>
    </slide>
    <slide style="background-image: url(/media/slider/slide5.jpg)">
      <div class="slide-content">
        <div class="caption">We<br>Produce.</div>
        <button class="btn btn-success btn-rounded btn-lg">Application/Products</button>
      </div>
    </slide>
  </carousel>  
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';

export default {
  components: {
    Carousel,
    Slide
  }
}
</script>

<style lang="scss">
.VueCarousel-slide {
  height: 645px;
  position: relative;
  background-size: cover;
  background-position: center center;
}
.slide-content {
  transform: translateY(-50%) translateX(-80%);
  position: absolute;
  left: 50%;
  right: 0;
  top: 50%;
  margin-top: 30px;

  .caption {
    font-size: rem(100);
    line-height: 1;
    color: #fff;
    font-weight: 700;
    text-transform: uppercase;
    margin-bottom: rem(30);
  }
}
.VueCarousel-navigation .VueCarousel-navigation-prev,
.VueCarousel-navigation .VueCarousel-navigation-next {
  transform: none;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  color: #fff;
  background-color: rgba(0,0,0,0.5);
  user-select: none;

  &:hover {
    background-color: rgba(0,0,0,1);
  }
}
.VueCarousel-navigation .VueCarousel-navigation-prev {
  left: 20px;
}
.VueCarousel-navigation .VueCarousel-navigation-next {
  right: 20px;
}
</style>
