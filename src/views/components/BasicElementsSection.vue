<template>
  <div class="wrapper">
    <div class="md-layout">
        <div class="md-layout-item md-size-66 mx-auto md-small-size-100">
          <md-card>
            <carousel
              :per-page="1"
              loop
              :speed="700"
              autoplay
              :autoplay-timeout="5000"
              :mouse-drag="false"
              navigationEnabled
              navigationNextLabel="<i class='material-icons'>keyboard_arrow_right</i>"
              navigationPrevLabel="<i class='material-icons'>keyboard_arrow_left</i>"
            >
              <slide>
                <!-- 이미지내 text
                <div class="carousel-caption">
                  <h4>
                    <md-icon>location_on</md-icon>
                    Somewhere Beyond, United States
                  </h4>
                </div> -->
                <img :src="carousel1" alt="carousel1" />
              </slide>
              <slide>
                <!-- 이미지내 text
                <div class="carousel-caption">
                  <h4>
                    <md-icon>location_on</md-icon>
                    Yellowstone National Park, United States
                  </h4>
                </div> -->
                <img :src="carousel2" alt="carousel2" />
              </slide>
              <slide>
                <!-- 이미지내 text
                <div class="carousel-caption">
                  <h4>
                    <md-icon>location_on</md-icon>
                    Yellowstone National Park, United States
                  </h4>
                </div> -->
                <img :src="carousel3" alt="carousel3" />
              </slide>
            </carousel>
          </md-card>
        </div>
      </div>
  

    

  </div>
</template>

<script>
// import { Pagination } from "@/components";
// import { Slider } from "@/components";
// import { Badge } from "@/components";

export default {
  // components: {
  //   Pagination,
  //   Slider,
  //   Badge
  // },
  data() {
    return {
      defaultPagination: 3,
      infoPagination: 3,
      initial: null,
      floatingLabel: null,
      success: null,
      error: null,
      withMIcon: null,
      withFaIcon: null,
      checkbox1: true,
      checkbox2: null,
      checkbox3: true,
      checkbox4: null,
      radio1: true,
      radio2: false,
      switch1: true,
      switch2: null,
      amount: 30,
      amount2: 60,
      buffer: 40,
      sliders: {
        simple: 40,
        rangeSlider: [20, 60]
      },
      carousel1: require("@/assets/img/octopus.jpg"),
      carousel2: require("@/assets/img/fish.jpg"),
      carousel3: require("@/assets/img/mix.jpg")
    };
  }
};
</script>

<style lang="scss" scoped>
.vertical-center {
  display: flex;
  align-items: center;
}
.flex-column {
  display: flex;
  flex-direction: column;
}
.md-checkbox,
.md-radio {
  display: flex;
  margin: 0;
  margin-bottom: 0.5rem;
}
</style>
