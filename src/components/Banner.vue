<template>
  <!-- eslint-disable -->
  <carousel
    :per-page="1"
    :mouse-drag="false"
    :autoplay="false"
    :autoplayTimeout="3000"
    :loop="true"
    :navigationEnabled="true"
    :paginationEnabled="false"
  >
    <!-- eslint-enable -->
    <slide style="background-image: url(/media/slider/slide1.jpg)">
      <div class="slide-content">
        <div class="caption">
          Steel
          <br />Cylinders.
        </div>
        <button class="btn btn-success btn-rounded btn-lg">Production</button>
      </div>
    </slide>
    <slide style="background-image: url(/media/slider/slide2.jpg)">
      <div class="slide-content">
        <div class="caption">
          With high
          <br />Pressure.
        </div>
        <button class="btn btn-success btn-rounded btn-lg">Quality Standards</button>
      </div>
    </slide>
    <slide style="background-image: url(/media/slider/slide3.jpg)">
      <div class="slide-content">
        <div class="caption">
          Because
          <br />We can.
        </div>
        <button class="btn btn-success btn-rounded btn-lg">Home</button>
      </div>
    </slide>
    <slide style="background-image: url(/media/slider/slide4.jpg)">
      <div class="slide-content">
        <div class="caption">
          Seamless
          <br />Safe.
        </div>
        <button class="btn btn-success btn-rounded btn-lg">Company</button>
      </div>
    </slide>
    <slide style="background-image: url(/media/slider/slide5.jpg)">
      <div class="slide-content">
        <div class="caption">
          We
          <br />Produce.
        </div>
        <button class="btn btn-success btn-rounded btn-lg">Application/Products</button>
      </div>
    </slide>
  </carousel>
</template>

<script>
export default {
  name: "Banner",
  components: {
    Carousel: () =>
      import("vue-carousel")
        .then(m => m.Carousel)
        .catch(),
    Slide: () =>
      import("vue-carousel")
        .then(m => m.Slide)
        .catch()
  }
};
</script>

<style lang="scss">
.VueCarousel-slide {
  height: 645px !important;
  position: relative !important;
  background-size: cover !important;
  background-position: center center !important;
}
.VueCarousel-navigation .VueCarousel-navigation-prev,
.VueCarousel-navigation .VueCarousel-navigation-next {
  transform: none !important;
  width: 40px !important;
  height: 40px !important;
  border-radius: 50% !important;
  color: #fff !important;
  background-color: rgba(0, 0, 0, 0.5) !important;
  user-select: none !important;

  &:hover {
    background-color: rgba(0, 0, 0, 1) !important;
  }
}
.VueCarousel-navigation .VueCarousel-navigation-prev {
  left: 20px !important;
}
.VueCarousel-navigation .VueCarousel-navigation-next {
  right: 20px !important;
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
</style>
